<properties
pageTitle="VM boot error"
description="虚拟机无法启动并出现错误代码 0xc0000001"
infoBubbleText="发现了启动错误。"
service="microsoft.compute"
resource="virtualmachines"
authors="Ram-Kakani"
displayOrder=""
articleId="VMCannotRDP-BootError-0xc0000001-BootBCD"
diagnosticScenario="booterror"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>


# <a name="vm-boot-error"></a>VM 启动错误
<!--issueDescription-->
## <a name="boot-error-found-for-your-virtual-machine---vmname--vmname--vmname--"></a>**发现了虚拟机 <!--$vmname-->[vmname]<!--/$vmname--> 的启动错误：**
Microsoft Azure 已调查完你的虚拟机 (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->。 我们发现，由于 Windows 无法启动并出现错误代码 **0xc0000001**，你的 VM 当前处于不可访问状态。 如果在启动配置数据中指定一个不存在的设备，则会发生此问题。<br>
<!--/issueDescription-->

## <a name="recommended-steps"></a>**建议的步骤**
若要修复 BCD 存储，请按照下面所述的故障排除步骤执行操作：

1. 删除虚拟机 <!--$vmname-->[vmname]<!--/$vmname-->。 执行此操作时，请确保选择“保留磁盘”选项。
2. 在继续保存 OS 磁盘的副本之前，选择此选项可帮助在恢复期间回滚。具体请参阅[为 Azure 中运行的专用 Windows VM 创建副本](https://docs.azure.cn/zh-cn/virtual-machines/windows/create-vm-specialized)
3. 将已删除的 VM 的 OS 磁盘作为数据磁盘附加到另一个 VM（故障排除 VM）。 有关详细信息，请参阅[如何在 Azure 门户中将数据磁盘附加到 Windows VM](https://docs.azure.cn/zh-cn/virtual-machines/windows/attach-disk-portal)。
4. 连接到故障排除 VM，确保新附加的 OS 磁盘已联机并分配有驱动器号。
5. 标识启动分区和 Windows 分区。 如果 OS 磁盘只包含一个分区，此分区即为启动分区和 Windows 分区。
  * Windows 分区包含名为“Windows”的文件夹，比其他分区大。
  * 启动分区包含名为“Boot”的文件夹。 此文件夹默认已隐藏。 若要查看该文件夹，必须显示已隐藏的文件和文件夹，并禁用“隐藏受保护的操作系统文件(推荐)”选项。 启动分区通常为 300 MB~500 MB
6. 以管理员身份运行以下命令行，然后记录 Windows 启动加载程序（不是 Windows 引导管理器）的标识符。 标识符是由 32 个字符构成的代码，类似于：xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx。  下一步骤要用到此标识符

      ```
      bcdedit /store [Boot partition]:\boot\bcd /enum
      ```
7. 运行以下命令行修复启动配置数据。 必须将以下占位符替换为实际值：
  * “Windows 分区”是包含名为“Windows”的文件夹的分区。
  * “启动分区”是包含名为“Boot”的隐藏系统文件夹的分区。
  * “标识符”是在上一步骤中找到的 Windows 启动加载程序的标识符。

        ```
          bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} device partition=[boot partition]:
          bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} integrityservices enable
          bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} device partition=[Windows partition]:
          bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} integrityservices enable
          bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} recoveryenabled Off
          bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} osdevice partition=[Windows partition]:
          bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
        ```

8. 从故障排除 VM 中分离已修复的 OS 磁盘。 [然后，从该 OS 磁盘创建新的 VM](https://docs.azure.cn/zh-cn/virtual-machines/windows/create-vm-specialized)


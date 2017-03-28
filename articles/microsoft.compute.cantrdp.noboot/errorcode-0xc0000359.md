<properties
pageTitle="VM boot error"
description="虚拟机无法启动并出现错误代码 0xC0000359"
infoBubbleText="发现了启动错误。"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="VMCannotRDP_A139226A-AD29-487A-80BE-4BD8CE6095CC"
diagnosticScenario="booterror"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>


# <a name="vm-boot-error"></a>VM 启动错误
<!--issueDescription-->
## <a name="boot-error-found-for-your-virtual-machine-vmname--vmname--"></a>**发现了虚拟机 [vmname] 的启动错误<!--($vmname)-->：**
Microsoft Azure 已调查完你的虚拟机 (VM) **[vmname]**<!--($vmname)-->。 我们发现，由于 Windows 无法启动并出现错误代码 **0xC0000359**，你的 VM 当前处于不可访问状态。 由于关键的系统驱动程序缺失或损坏，无法加载操作系统。<br>
<!--/issueDescription-->

## <a name="recommended-steps"></a>**建议的步骤**
若要解决该问题，请遵循以下故障排除步骤将 OS 磁盘附加到另一个 VM，然后使用同一台计算机上 C:\windows\WinSxS 文件夹中的文件或者具有相同 OS 和修补程序级别的其他正常 VM 上的文件，来替换已损坏的文件。

1. 请记下屏幕截图中所示的文件名和路径。
2. 删除虚拟机 [vmname]<!--($vmname)-->。 执行此操作时，请确保选择“保留磁盘”选项。
3. 在继续保存 OS 磁盘的副本之前，选择此选项可帮助在恢复期间回滚。具体请参阅[为 Azure 中运行的专用 Windows VM 创建副本](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy)
4. 将已删除的 VM 的 OS 磁盘作为数据磁盘附加到另一个 VM（故障排除 VM）。 有关详细信息，请参阅[如何在 Azure 门户中将数据磁盘附加到 Windows VM](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal)。
5. 连接到故障排除 VM，确保新附加的 OS 磁盘已联机并分配有驱动器号。
6. 标识启动分区和 Windows 分区。 如果 OS 磁盘只包含一个分区，此分区即为启动分区和 Windows 分区。
  * Windows 分区包含名为“Windows”的文件夹，比其他分区大。
  * 启动分区包含名为“Boot”的文件夹。 此文件夹默认已隐藏。 若要查看该文件夹，必须显示已隐藏的文件和文件夹，并禁用“隐藏受保护的操作系统文件(推荐)”选项。 启动分区通常为 300 MB~500 MB
7. 在附加的 OS 磁盘中，浏览到步骤 1 中记下的文件路径，然后将该文件重命名为 [BINARY.SYS].OLD。
8. 现在，请在权限提升的命令提示符下找到 Windows 目录所在的卷，浏览到 \windows\winsxs，然后搜索屏幕截图中所示的二进制文件。 以下命令返回计算机上所有的不同版本文件。
```
  dir [binary name without the extension]* /s
```
9. 请选择列表中的最新条目，然后将它复制到附加的 OS 磁盘上的 windows\system32 文件夹路径。
```
  copy [drive]:\Windows\WinSxS\[directory_where_file_is]\[binary_with_extension] [drive]:\Windows\System32\Drivers\   
```
10. 如果找不到其他可用于替换的文件，请在具有相同 OS 版本和修补程序级别的计算机上（如果可能）找到相应的二进制文件，然后替换受影响计算机上已损坏的二进制文件。
11. 从故障排除 VM 中分离已修复的 OS 磁盘。 [然后，从该 OS 磁盘创建新的 VM](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-create-vm-specialized)


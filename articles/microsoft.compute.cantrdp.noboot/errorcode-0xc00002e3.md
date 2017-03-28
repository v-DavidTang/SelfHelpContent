<properties
pageTitle="VM in reboot loop"
description="虚拟机无法启动并出现错误代码 0xC00002E3"
infoBubbleText="发现 VM 处于重新启动循环中。"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="VMCannotRDP_FFE84A13-177A-4524-8BD7-3D13E8048893"
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
Microsoft Azure 已调查完你的虚拟机 (VM) **[vmname]**<!--($vmname)-->。 我们发现，由于你的 VM 处于重新启动循环中并出现错误代码 **0xC00002E3**，因此当前处于不可访问状态。 如果 SAM 注册表配置单元缺失或损坏，则会发生该问题。<br>
<!--/issueDescription-->

## <a name="recommended-steps"></a>**建议的步骤**
若要解决该问题，请遵循以下故障排除步骤将 OS 磁盘附加到另一个 VM，然后使用同一台计算机上 C:\windows\WinSxS 文件夹中的文件或者具有相同 OS 和修补程序级别的其他正常 VM 上的文件，来替换已损坏的文件。

1. 请记下屏幕截图中所示的文件名和路径。
2. 删除虚拟机 [vmname]<!--($vmname)-->。 执行此操作时，请确保选择“保留磁盘”选项。
3. 在继续保存 OS 磁盘的副本之前，选择此选项可帮助在恢复期间回滚。具体请参阅[为 Azure 中运行的专用 Windows VM 创建副本](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy)
4. 将已删除的 VM <!--($vmname)--> 的 OS 磁盘作为数据磁盘附加到另一个 VM（故障排除 VM）。 有关详细信息，请参阅[如何在 Azure 门户中将数据磁盘附加到 Windows VM](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal)。
5. 连接到故障排除 VM，确保新附加的 OS 磁盘已联机并分配有驱动器号。
6. 标识启动分区和 Windows 分区。 如果 OS 磁盘只包含一个分区，此分区即为启动分区和 Windows 分区。
  * Windows 分区包含名为“Windows”的文件夹，比其他分区大。
  * 启动分区包含名为“Boot”的文件夹。 此文件夹默认已隐藏。 若要查看该文件夹，必须显示已隐藏的文件和文件夹，并禁用“隐藏受保护的操作系统文件(推荐)”选项。 启动分区通常为 300 MB~500 MB
7. 浏览到文件夹 \windows\system32\config，检查文件 SAM 是否存在，如果存在，请将它重命名为 SAM.CORRUPT。
8. 如果在 VM 出现此问题之前你已备份磁盘或已创建系统备份，请检查 \windows\system32\config 中是否存在 SAM 文件。
9. 如果备份中存在 SAM 文件，请使用该文件替换或者将它复制到受影响计算机的 OS 磁盘中的 \windows\system32\config 文件夹。
10. 如果未创建备份文件，请在受影响的磁盘上，将 \windows\system32\config\regback\SAM 中的复制到 \windows\system32\config\。
11. 从故障排除 VM 中分离已修复的 OS 磁盘。 [然后，从该 OS 磁盘创建新的 VM](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-create-vm-specialized)


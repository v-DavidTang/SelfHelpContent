<properties
    pageTitle="VM boot error"
    description="Linux VM 等待输入"
    infoBubbleText="发现了 fstab 问题"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="craigwiand"
    displayOrder="1"
    articleId="VMCannotSSH_D798E6ED-7353-480D-8825-51C2729DD5BA"
    diagnosticScenario="CantSSH"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="linux"
    productPesIds="15571"
    cloudEnvironments="public"
/>


# <a name="diagnostics-on-your-linux-virtual-machine-found-a-boot-error"></a>在 Linux 虚拟机上执行的诊断发现了启动错误 
<!--issueDescription-->
## <a name="boot-error-found-for-your-virtual-machine---vmname--vmname--vmname--"></a>**发现了虚拟机 <!--$vmname-->[vmname]<!--/$vmname--> 的启动错误：**
Microsoft Azure 已调查完你的虚拟机 (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->。 我们发现，由于你的 VM 正在等待用户输入以继续执行启动过程，因此当前处于不可访问状态。  此问题通常是由文件系统表 (fstab) 文件中的某个问题造成的。  

若要查看更多详细信息，请在门户中的“启动诊断”边栏选项卡上查看串行日志输出，路径如下：**虚拟机** > <!--$vmname-->**[vmname]**<!--/$vmname--> > **所有设置** > **启动诊断**
<!--/issueDescription-->
   
## <a name="recommended-steps"></a>**建议的步骤**
若要恢复该虚拟机，请遵循以下步骤：

1. 将 OS 磁盘附加到恢复 VM。 若要执行此操作，请查看以下 Azure 文章，并遵循从最开头到*修复原始虚拟硬盘上的问题*部分的所有步骤：[通过使用 Azure CLI 将 OS 磁盘附加到恢复 VM 来对 Linux VM 进行故障排除](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-troubleshoot-recovery-disks)。

2. 在新 VM 上将 OS 磁盘装载为数据磁盘后，请在恢复 VM 上使用文本编辑器更正 fstab 文件。 有关更正 Azure Linux 虚拟机中 fstab 问题的详细信息，请参阅：[Azure Linux VM 由于 fstab 错误而无法启动](https://support.microsoft.com/help/3206699)。

3. 解决 fstab 问题后，返回到[通过使用 Azure CLI 将 OS 磁盘附加到恢复 VM 来对 Linux VM 进行故障排除](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-troubleshoot-recovery-disks)，然后重新参阅*卸载并分离原始虚拟硬盘*部分中的步骤来重新创建原始 VM。


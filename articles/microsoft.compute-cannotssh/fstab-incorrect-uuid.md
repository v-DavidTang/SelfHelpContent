<properties
    pageTitle="VM boot error"
    description="fstab 中的 UUID 不正确"
    infoBubbleText="发现了 fstab 问题"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="craigwiand"
    displayOrder="1"
    articleId="VMCannotSSH_72059703-AD61-42AF-BF8A-991A7DEFA197"
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
Microsoft Azure 已调查完你的虚拟机 (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->。 我们发现，由于文件系统表 (fstab) 文件包含的某个条目使用了 VM 上不存在的文件系统的全局唯一标识符 (UUID)，因此你的 VM 当前处于不可访问状态。  有多种原因可能会造成这种情况，包括删除了数据磁盘，或者在未更新 /etc/fstab 文件的情况下重新启动。  

若要查看更多详细信息，请在门户中的“启动诊断”边栏选项卡上查看串行日志输出，路径如下：**虚拟机** > <!--$vmname-->**[vmname]**<!--/$vmname--> > **所有设置** > **启动诊断**
<!--/issueDescription-->
   
## <a name="recommended-steps"></a>**建议的步骤**
若要恢复该虚拟机，请遵循以下步骤：

1. 将 OS 磁盘附加到恢复 VM。 若要执行此操作，请查看以下 Azure 文章，并遵循从最开头到*修复原始虚拟硬盘上的问题*部分的所有步骤：[通过使用 Azure CLI 将 OS 磁盘附加到恢复 VM 来对 Linux VM 进行故障排除](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-troubleshoot-recovery-disks)。

2. 在新 VM 上将 OS 磁盘装载为数据磁盘后，请在恢复 VM 上使用文本编辑器更正 fstab 文件。 有关更正 Azure Linux 虚拟机中 fstab 问题的详细信息，请参阅：[Azure Linux VM 由于 fstab 错误而无法启动](https://support.microsoft.com/help/3206699)。

3. 解决 fstab 问题后，返回到[通过使用 Azure CLI 将 OS 磁盘附加到恢复 VM 来对 Linux VM 进行故障排除](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-troubleshoot-recovery-disks)，然后重新参阅*卸载并分离原始虚拟硬盘*部分中的步骤来重新创建原始 VM。



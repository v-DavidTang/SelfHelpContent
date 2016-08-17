<properties
    pageTitle="azure iaas vm backup/register or back up a linux virtual machine"
    description="Azure IAAS VM 备份/注册或备份 Linux 虚拟机"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="kasparks"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32447378"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# Azure IAAS VM 备份/注册或备份 Linux 虚拟机
## **建议的步骤**
若要解决大多数常见问题，请尝试下面的一个或多个步骤。
* 检查安装的 VM 代理是否是最新的。 <br>
[更新 Linux VM 代理](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-2-the-microsoft-azure-vm-agent-installed-in-the-vm-is-out-of-date-for-linux-vms)

* 确保 VM 可以访问 Internet 来创建快照 <br>
[为 NSG 或防火墙下的虚拟机启用 Internet 访问](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-1-the-vm-does-not-have-internet-access)

* 检查 VMSnapshotLinux 扩展是否是最新的 <br>
[确保使用最新扩展的步骤](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-3-the-backup-extension-fails-to-update-or-load)

* VM 备份速度缓慢 <br>
[影响备份时间的因素](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-introduction/#total-vm-backup-time)

* 检查你是否遵循了有关优化备份性能的最佳实践 <br>
[获得最佳备份性能的最佳实践](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-introduction/#best-practices)

## **建议的文档**
[Azure 虚拟机备份故障排除指南](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-troubleshoot/)



<!--HONumber=Aug16_HO1-->



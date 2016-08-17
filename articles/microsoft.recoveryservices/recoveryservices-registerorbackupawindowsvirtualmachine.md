<properties
    pageTitle="azure iaas vm backup/register or back up a windows virtual machine"
    description="Azure IAAS VM 备份/注册或备份 Windows 虚拟机"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="kasparks"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32447379"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# Azure IAAS VM 备份/注册或备份 Windows 虚拟机

## **建议的步骤**
若要解决大多数常见问题，请尝试下面的一个或多个步骤。
* 确保 VM 可以访问 Internet 来创建快照[为 NSG 或防火墙下的虚拟机启用 Internet 访问。](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-1-the-vm-does-not-have-internet-access)

* 检查 VMSnapshot 扩展是否是最新的[确保使用最新扩展的步骤](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-3-the-backup-extension-fails-to-update-or-load)

* 检查是否可以检索所创建的快照的状态[确保可检索快照状态的步骤](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-4-the-snapshots-status-cannot-be-retrieved-or-the-snapshots-cannot-be-taken)

* VM 备份速度缓慢[影响备份时间的因素](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-introduction/#total-vm-backup-time)

* 检查你是否遵循了有关优化备份性能的最佳实践[获得最佳备份性能的最佳实践](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-introduction/#best-practices)

## **建议的文档**
[Azure 虚拟机备份故障排除指南](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-troubleshoot/)



<!--HONumber=Aug16_HO1-->



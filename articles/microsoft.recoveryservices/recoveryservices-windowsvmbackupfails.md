<properties
    pageTitle="备份 Windows VM 失败并出现“无法与 VM 代理通信，因此无法获取快照状态”"
    description="Windows VM 快照问题"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="trinadhk"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 备份 Windows VM 失败并出现“无法与 VM 代理通信，因此无法获取快照状态”

## **建议的步骤**
若要解决常见问题，请尝试以下一个或多个步骤。

1. 检查 VM 是否可以访问 Internet 来创建快照。 了解当 VM 位于 NSG 或防火墙后面时如何[启用 Internet 访问](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-1-the-vm-does-not-have-internet-access)。 
2. 检查 VMSnapshot 扩展（备份使用的扩展）是否是[最新的](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-3-the-backup-extension-fails-to-update-or-load)
3. 检查快照状态是否为[可检索](https://azure.microsoft.com/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-4-the-snapshots-status-cannot-be-retrieved-or-the-snapshots-cannot-be-taken)。


## **建议的文档**
[Azure 虚拟机备份故障排除指南](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)<br>



<!--HONumber=Jul16_HO3-->



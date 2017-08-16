<properties
    pageTitle="My SQL Server VM is slow"
    description="SQL Server VM 运行速度缓慢"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="michco"
    displayOrder="25"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="WindowsSQL"
    productPesIds="14749"
    cloudEnvironments="public"
/>
    

# SQL Server VM 运行速度缓慢

## **建议的步骤**
尝试执行以下步骤来诊断和解决 SQL VM 性能问题。

1. 为生产工作负荷使用高级存储，并启用读取缓存（将“主机缓存”选项设置为“只读”）<br>
[高级存储文档](https://docs.azure.cn/zh-cn/storage/storage-premium-storage/)
2. 查看性能最佳实践<br>
[Azure 虚拟机中 SQL Server 的性能最佳实践](https://docs.azure.cn/zh-cn/virtual-machines/windows/sql/virtual-machines-windows-sql-performance/)
3. 排查一般的 SQL Server 工作负荷性能问题：<br>
[SQL Server 性能：方法和工具](https://docs.com/ajith-krishnan/8919/sql-server-performance-troubleshooting-approach)

## **建议的文档**
[在 Azure 门户中预配 SQL Server 虚拟机](https://docs.azure.cn/zh-cn/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-server-provision/)<br>
[迁移到 Azure 高级存储](https://docs.azure.cn/zh-cn/storage/storage-migration-to-premium-storage/)


<!--HONumber=Jul16_HO3-->



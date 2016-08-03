<properties
    pageTitle="性能/数据库服务器速度缓慢或无响应"
    description="性能/数据库服务器速度缓慢或无响应"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32511138"
    resourceTags="windowsSQL"
    productPesIds="14745"
    cloudEnvironments="public"
/>


# 性能/数据库服务器速度缓慢或无响应

## **建议的步骤**
尝试执行以下步骤来诊断和解决 SQL VM 性能问题

1. 为生产工作负荷使用高级存储，并启用读取缓存（将“主机缓存”选项设置为“只读”）<br>
[高级存储文档](https://azure.microsoft.com/documentation/articles/storage-premium-storage/)
2. 查看性能最佳实践<br>
[Azure 虚拟机中 SQL Server 的性能最佳实践](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-performance/)
3. 排查一般的 SQL Server 工作负荷性能问题：<br>
[SQL Server 性能：方法和工具](https://docs.com/ajith-krishnan/8919/sql-server-performance-troubleshooting-approach)
4. 注意：在门户和 Azure Resource Manager 模型中创建的 SQL Server VM 将实施性能最佳实践

## **建议的文档**
[Azure 虚拟机中 SQL Server 的性能最佳实践](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-performance/)<br>
[高级存储： 适用于 Azure 虚拟机工作负荷的高性能存储](https://azure.microsoft.com/documentation/articles/storage-premium-storage/)<br>
[SQL Server 性能：方法和工具](https://docs.com/ajith-krishnan/8919/sql-server-performance-troubleshooting-approach)<br>
[Microsoft Azure 虚拟机中的 SQL Server 的性能指南](http://download.microsoft.com/download/D/2/0/D20E1C5F-72EA-4505-9F26-FEF9550EFD44/Performance Guidance for SQL Server in Windows Azure Virtual Machines.docx)



<!--HONumber=Jul16_HO4-->



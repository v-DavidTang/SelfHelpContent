<properties
    pageTitle="设置和配置/升级 SQL VM 或 SQL 版本"
    description="设置和配置/升级 SQL VM 或 SQL 版本"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32511160"
    resourceTags="windowsSQL"
    productPesIds="14745"
    cloudEnvironments="public"
/>


# 设置和配置/升级 SQL VM 或 SQL 版本

## **建议的步骤**
1. 升级到新版本：目前，在 Azure VM 中运行的 SQL Server 无法就地升级。 因此，请使用所需的 SQL Server 版本创建新的 Azure 虚拟机，然后使用标准数据迁移技术，将数据库迁移到新的服务器。<br>
[将 SQL Server 数据库迁移到 Azure VM 中的 SQL Server](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-migrate-sql/)
2. 应用更新和服务包：虚拟机允许你控制主机，包括应用更新的时间与方法。 对于操作系统，可以手动应用 Windows 更新，或者启用名为“自动修补”的计划服务。 自动修补将安装任何标记为重要的更新，包括该类别中的 SQL Server 更新。 必须手动安装其他可选的 SQL Server 更新。<br>
[Azure 虚拟机中 SQL Server 的自动修补 (Resource Manager)](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-automated-patching/)

## **建议的文档**
[Azure 虚拟机中的 SQL Server 常见问题](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-server-iaas-faq/?rnd=1)



<!--HONumber=Jul16_HO4-->



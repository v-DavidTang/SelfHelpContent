<properties
    pageTitle="在服务器或订阅之间迁移，或者向/从 Azure 迁移"
    description="在服务器或订阅之间迁移，或者向/从 Azure 迁移"
    service="microsoft.sql"
    resource="servers"
    authors="kasparks"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servers, databases"
    productPesIds=""
    cloudEnvironments="public"
/>


# 在服务器或订阅之间迁移，或者向/从 Azure 迁移

## **建议的步骤**
以下详细信息说明如何迁移或移动数据库。

* 将数据库移到同一订阅中的不同服务器。<br>
在 SQL 数据库资源边栏选项卡顶部单击“复制”。
* 在订阅之间移动逻辑服务器。 注意：无法直接在订阅之间移动数据库。<br>
在包含你的数据库的 SQL server 资源边栏选项卡顶部单击“移动”，然后选择要移动的资源以及要移到的订阅。
* 若要将现有 SQL 数据库迁移到 Azure，请先运行兼容性工具以确定是否可迁移该数据库，解决所有不兼容问题，然后选择适当的迁移方法。<br>
[将 SQL Server 数据库迁移到 Azure SQL](https://azure.microsoft.com/documentation/articles/sql-database-cloud-migrate/)
* 创建数据库的副本以便在 Azure 外部使用该数据库。<br>
[导出 BACPAC 文件](https://azure.microsoft.com/documentation/articles/sql-database-export/)

## **建议的文档**
[在服务器之间或订阅之间移动数据库，以及将数据库移入和移出 Azure](http://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-moving-data/)<br>
[如何复制 Azure SQL 数据库](http://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-moving-data/)



<!--HONumber=Jun16_HO3-->



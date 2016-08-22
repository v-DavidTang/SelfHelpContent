<properties
    pageTitle="Backing up and restoring databases"
    description="备份和还原数据库"
    service="microsoft.sql"
    resource="servers"
    authors="kasparks"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32302682"
    resourceTags="databases, servers"
    productPesIds="13491"
    cloudEnvironments="public"
/>


# 备份和还原数据库

## **建议的步骤**
SQL 数据库保留了你数据库的副本，因此你可以在发生服务中断和用户错误的情况下进行恢复。 这包括将数据库还原到以前的时间点、还原已删除的数据库，或者在数据中心服务中断的情况下进行恢复。 可用的选项取决于数据库服务层和你选择的选项。 还原数据库后，请确保在将最近恢复的 Azure SQL 数据库部署回到生产环境之前，浏览最终任务的清单。

* 将数据库还原到以前的时间点。<br>
在所选 SQL 数据库的资源边栏选项卡顶部单击“还原”以打开“还原”边栏选项卡，然后填写所需的详细信息。
* 还原意外删除的数据库。<br>
在“操作”下方的 SQL Server 资源边栏选项卡底部单击“已删除的数据库”磁贴以启动还原过程。
* 从异地冗余的备份还原为新数据库（也称异地还原）。<br>
依次单击“新建”、“数据和存储”、“SQL 数据库”，然后在源列表中选择“备份”。
* 针对已还原的数据库完成最终任务清单<br>
[最终确定已还原的数据库](https://azure.microsoft.com/documentation/articles/sql-database-recovered-finalize/)
* 从 Azure 数据库备份中还原单个表。<br>
[如何从 Azure SQL 数据库备份中还原单个表](https://azure.microsoft.com/documentation/articles/sql-database-cloud-migrate-restore-single-table-azure-backup/)

## **建议的文档**
[将数据库还原到以前的时间点、还原已删除的数据库，或者在数据中心服务中断的情况下进行恢复](https://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-backup-and-restore/)<br>
[业务连续性概述](https://azure.microsoft.com/documentation/articles/sql-database-business-continuity/)<br>
[业务连续性设计](https://azure.microsoft.com/documentation/articles/sql-database-business-continuity-design/)



<!--HONumber=Aug16_HO2-->



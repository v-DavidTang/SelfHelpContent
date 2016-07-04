<properties
    pageTitle="How to recover from a backup"
    description="如何从备份中恢复"
    service="microsoft.sql"
    resource="servers"
    authors="kasparks"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="datawarehouse"
    productPesIds=""
    cloudEnvironments="public"
/>


# 如何从备份中恢复

## **建议的步骤**
SQL 数据仓库会自动创建数据仓库的快照，以便在发生服务中断和用户错误时能够恢复。  它允许你将数据仓库还原到以前的时间点、还原已删除的数据仓库，或者在数据中心服务中断后进行恢复。  还原数据仓库后，请确保在将最近恢复的 SQL 数据仓库部署回到生产环境之前，浏览最终任务的清单。

1. 若要还原数据仓库，请转到数据仓库的 Azure 门户页，打开“还原”边栏选项卡并填入所需的详细信息。
2. 若要还原已删除的数据仓库，请在“操作”下方的 SQL Server 还原边栏选项卡底部单击“已删除的数据库”磁贴以启动还原过程。

## **建议的文档**
[最终确定已还原的数据库](https://azure.microsoft.com/documentation/articles/sql-database-recovered-finalize/)<br>
[有关数据保护的详细信息](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-restore-database-overview/)



<!--HONumber=Jun16_HO5-->



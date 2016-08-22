<properties
    pageTitle="My database is slow"
    description="我的数据库运行速度缓慢"
    service="microsoft.sql"
    resource="servers"
    authors="kasparks"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds="31980430, 31980438"
    resourceTags="databases, servers"
    productPesIds="13491"
    cloudEnvironments="public"
/>


# 我的数据库运行速度缓慢

## **建议的步骤**
缺少索引与查询优化不足是数据库性能不佳的常见原因。 首先，使用以下链接通过“Query Performance Insight”和“索引顾问工具”来确定是否有机会微调这些索引与查询。 如果问题仍然存在，请考虑更改单一数据库的服务层，或者随时增加弹性数据库池的 eDTU 以提高性能。

* 使用 [Query Performance Insight](data-blade:SqlAzureExtension.QueryPerformanceBlade) 查找消耗最高的查询，并识别要修复的查询。
* 使用 [SQL 数据库顾问](data-blade:SqlAzureExtension.DatabaseRecommendationBlade)获取索引建议并创建索引。
* 分析 SQL Server 资源边栏选项卡上显示的度量值，以识别是否有任何资源被过度使用或受到限制。 通过纵向或横向扩展来缓解资源问题。<br>
[了解每个服务层中有哪些可用资源](https://azure.microsoft.com/documentation/articles/sql-database-service-tiers/)
* 对于多个数据库，可以使用弹性数据库池自动缩放资源。<br>
[了解弹性数据库池](https://azure.microsoft.com/documentation/articles/sql-database-elastic-pool-guidance/)

## **建议的文档**
[排查 Azure SQL 数据库性能问题](https://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-performance/)<br>
[使用 DMV 进行监视](https://azure.microsoft.com/documentation/articles/sql-database-monitoring-with-dmvs/)<br>
[扩展事件](https://azure.microsoft.com/documentation/articles/sql-database-xevent-db-diff-from-svr/)<br>
[基准概述](https://azure.microsoft.com/documentation/articles/sql-database-benchmark-overview/)



<!--HONumber=Aug16_HO2-->



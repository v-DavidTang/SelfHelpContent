<properties
    pageTitle="How to improve and debug performance"
    description="如何改进和调试性能"
    service="microsoft.sql"
    resource="servers"
    authors="kasparks"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="datawarehouse"
    productPesIds=""
    cloudEnvironments="public"
/>


# 如何改进和调试性能

## **建议的步骤**
若要解决最常见的性能问题，请尝试以下方法。

1. 扩展和缩减 SQL 数据仓库的操作非常简单，可将计算能力暴增较短的一段时间，或者长期提升性能。  如果你刚开始使用不久或者最近增加了所要处理的数据量，我们建议尝试使用多种 DWU 设置，以了解哪种设置最适合你。<br>
[了解有关缩放和 DWU 的详细信息](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-manage-compute-overview/)
2. 缩放 SQL 数据仓库可能会影响并发。  了解如何使用资源类管理并发。<br>
[资源类](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-develop-concurrency/)
3. 请查看我们的 SQL 数据仓库最佳实践，其中提供了有关快速顺畅地运行实例的多项提示。<br>
[SQL 数据仓库最佳实践](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-best-practices/)

## **建议的文档**
[使用 DMV 调查查询](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-manage-monitor/)<br>
[更多故障排除方法](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)



<!--HONumber=Jun16_HO5-->



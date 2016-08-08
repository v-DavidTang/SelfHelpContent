<properties
    pageTitle="I need more storage/throughput"
    description="我需要更大的存储空间/吞吐量"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="AndrewHoh"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 我需要更大的存储空间/吞吐量

## **建议的步骤**
尝试采取下面最适合你当前方案的建议措施。

* 我正在使用预定义的性能集合（**S1**、**S2** 或 **S3**），并想要改用用户定义的性能，以便能够单独设置存储和吞吐量选项。
你可以遵循这些[说明](https://azure.microsoft.com/documentation/articles/documentdb-performance-levels/#changing-performance-levels-using-the-azure-portal)，使用门户将定价层更改为**标准**
* 我正在使用单分区集合或预定义的性能集合，并想要改用分区的集合。
你可以遵循这些[说明](https://azure.microsoft.com/documentation/articles/documentdb-partition-data/#_migrating-from-single-partition-to-partitioned-collections)，使用 DocumentDB 数据迁移工具将数据从单分区集合（**S1**、**S2**、**S3** 或 **标准**）迁移到分区的集合
* 我只想要增大当前集合的吞吐量。
你可以遵循这些[说明](https://azure.microsoft.com/documentation/articles/documentdb-performance-levels/#change-throughput)，使用门户来更改吞吐量

## **建议的文档**
[从单个分区集合迁移到已分区集合](https://azure.microsoft.com/documentation/articles/documentdb-partition-data/#_migrating-from-single-partition-to-partitioned-collections)<br>
[为 DocumentDB 中的数据建模](https://azure.microsoft.com/documentation/articles/documentdb-modeling-data/)<br>
[DocumentDB 中的性能级别](https://azure.microsoft.com/documentation/articles/documentdb-performance-levels/)



<!--HONumber=Aug16_HO1-->



<properties
    pageTitle="My queries are slow"
    description="查询速度缓慢"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="AndrewHoh"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 查询速度缓慢

## **建议的步骤**
若要加速查询，请尝试下面的一个或多个步骤。

* 尽可能避免对集合进行完整扫描。 所有用户定义的函数 (UDF) 和内置函数都会扫描查询范围内的所有文档；例如，*SELECT * FROM c* 的查询范围比 *SELECT * FROM c.foo = 'bar'* 更宽。 若要优化性能，请在包含 UDF 和内置函数的查询中添加 WHERE 子句，以缩小查询范围。<br>[DocumentDB 中的 SQL 查询和 SQL 语法 - 内置函数](https://azure.microsoft.com/documentation/articles/documentdb-sql-query/#built-in-functions)<br>[DocumentDB 中的 SQL 查询和 SQL 语法 - Where 子句](https://azure.microsoft.com/documentation/articles/documentdb-sql-query/#where-clause)
* 配置连接策略时使用直接模式作为连接模式。<br>[DocumentDB 性能提示 - 直接连接](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#direct-connection)
* 使用 x-ms-max-item-count 标头优化查询和读取源的页面大小，以提高性能。<br>[DocumentDB 性能提示 - 优化页面大小](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#tune-page-size)
* 对于已分区的集合，可以并行执行查询以提高性能并利用更大的吞吐量。<br>[
适用于 .NET SDK 1.9.2 和更高版本的 GitHub DocumentDB .NET 示例代码](https://github.com/Azure/azure-documentdb-dotnet/blob/master/samples/code-samples/Queries/Program.cs#L664-L734)

## **建议的文档**
[DocumentDB 性能提示](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/)<br>
[DocumentDB 中的 SQL 查询和 SQL 语法](https://azure.microsoft.com/documentation/articles/documentdb-sql-query/)



<!--HONumber=Aug16_HO1-->



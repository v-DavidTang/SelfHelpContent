<properties
    pageTitle="My database is slow"
    description="我的数据库运行速度缓慢"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="AndrewHoh"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 我的数据库运行速度缓慢

## **建议的步骤**
若要加速数据库，请尝试下面的一个或多个步骤。

* 安装最新的 DocumentDB SDK。 DocumentDB SDK 正在不断改进，以求提供最佳性能。<br>
[DocumentDB SDK](https://azure.microsoft.com/documentation/articles/documentdb-sdk-dotnet/)
* 配置连接策略时使用直接模式作为连接模式。<br>[DocumentDB 性能提示 - 直接连接](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#direct-connection)
* 增加线程/任务的数目，以减少完成请求所需的等待时间。<br>[DocumentDB 性能提示 - 增加线程](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#increase-threads)
* 对于.NET，请增大 *System.Net MaxConnections*，以便同时与 DocumentDB 建立多个连接。对于 .NET SDK 1.8.0 和更高版本，默认有 50 个线程。<br>[DocumentDB 性能提示 - 最大连接数](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#max-connection)
* 如果可能，请将你的应用程序和 DocumentDB 数据库部署到同一个 Azure 区域。 通过大致的比较发现，在同一区域中对 DocumentDB 的调用可在 1-2 毫秒内完成，而美国西岸和美国东岸之间的延迟则大于 50 毫秒。<br>[DocumentDB 性能提示 - 相同的区域](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#same-region)
* 尝试为集合增加分配的请求单位 (RU) 数目。<br>[DocumentDB 中的性能级别 - 更改集合的吞吐量](https://azure.microsoft.com/documentation/articles/documentdb-performance-levels/#change-throughput)

## **建议的文档**
[使用 Azure DocumentDB 进行性能和规模测试](https://azure.microsoft.com/documentation/articles/documentdb-performance-testing/)



<!--HONumber=Aug16_HO1-->



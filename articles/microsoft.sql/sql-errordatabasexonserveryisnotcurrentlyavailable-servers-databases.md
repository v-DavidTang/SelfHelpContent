<properties
    pageTitle="Error: Database <x> on server <y> is not currently available"
    description="错误：服务器 <y> 上的数据库 <x> 当前不可用"
    service="microsoft.sql"
    resource="servers"
    authors="kasparks"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servers, databases"
    productPesIds=""
    cloudEnvironments="public"
/>

# 错误：服务器 <y> 上的数据库 <x> 当前不可用

## **建议的步骤**
当 Azure SQL 数据库由于部署、故障转移或负载平衡而移动后，出现“无法连接”消息（错误代码 40613）。 这是一个暂时性的连接问题，因为重新配置通常会在 60 秒内完成。

* 连接到云服务的应用程序应编码为捕获定期连接错误（例如 40613），并且应实施重试逻辑。<br>
[针对暂时性错误的重试逻辑](https://azure.microsoft.com/documentation/articles/sql-database-connectivity-issues/#retry-logic-for-transient-errors)

## **建议的文档**
[排查“服务器 y 上的数据库 x 当前不可用。 请稍后重试连接”错误。](https://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-connection)


<!--HONumber=Jun16_HO3-->



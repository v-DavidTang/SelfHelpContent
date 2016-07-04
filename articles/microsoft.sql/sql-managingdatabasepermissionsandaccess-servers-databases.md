<properties
    pageTitle="Managing database permissions and access"
    description="管理数据库权限和访问"
    service="microsoft.sql"
    resource="servers"
    authors="kasparks"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servers, databases"
    productPesIds=""
    cloudEnvironments="public"
/>


# 管理数据库权限和访问

## **建议的步骤**
以下详细信息说明如何在 Azure SQL 数据库中设置和更新通用访问与权限规则。

* 更改逻辑服务器的管理密码。<br>
在 SQL Server 资源边栏选项卡顶部单击“重置密码”。
* 更新有权访问服务器和数据库的 IP 地址。<br>
[如何：在 SQL 数据库上配置防火墙设置](https://azure.microsoft.com/documentation/articles/sql-database-configure-firewall-settings/)
* 创建包含或隔离的数据库用户。<br>
[包含的数据库用户 - 使你的数据库可移植](https://msdn.microsoft.com/library/ff929188.aspx)
* 为包含的数据库用户设置基于 Azure Active Directory 的身份验证。<br>
[使用 Azure Active Directory 身份验证连接到 SQL 数据库](https://azure.microsoft.com/documentation/articles/sql-database-aad-authentication/)
* 设置其他用户或登录名以便对 master 数据库进行高特权访问。<br>
[在 Azure SQL 数据库中管理数据库和登录名](https://azure.microsoft.com/documentation/articles/sql-database-manage-logins/)

## **建议的文档**
[排查常见的 Azure SQL 数据库权限和访问问题](http://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-permissions/)<br>
[Azure SQL 数据库安全指导原则和限制](http://azure.microsoft.com/documentation/articles/sql-database-security-guidelines/)



<!--HONumber=Jun16_HO5-->



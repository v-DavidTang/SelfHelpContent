<properties
    pageTitle="open source technologies/mysql"
    description="开源技术/mysql"
    service="microsoft.web"
    resource="sites"
    authors="cts-shrahman"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32444077"
    resourceTags=""
    productPesIds="14748, 16170"
    cloudEnvironments="public"
/>


# 开源技术/MySQL

## **建议的步骤**
问题：站点上出现错误：“连接到数据库时出错”或“建立数据库连接时出错”，或者通过 PHPMyAdmin 连接到应用中的 MySQL 时出现“设置无效”消息。 

解决方法： 

1. 登录到 Azure 门户，浏览到应用服务，然后在“设置”部分下选择“应用程序设置”。
2. 在“应用设置”中，添加如下所示的键值项：

    
    键：WEBSITE_MYSQL_ARGUMENTS <br>
    值：--default_password_lifetime=0 
    

相关详细信息，请访问[此处](http://bit.ly/2dXlqMy)的论坛文章。 


## **建议的文档**

[宣布推出 Azure 应用服务 MySQL 应用内产品（预览版）](https://azure.microsoft.com/blog/mysql-in-app-preview-app-service/)<br>
[MySQL 应用内产品 Wiki](https://github.com/projectkudu/kudu/wiki/MySQL-in-app-(preview))<br>


<!--HONumber=Oct16_HO4-->



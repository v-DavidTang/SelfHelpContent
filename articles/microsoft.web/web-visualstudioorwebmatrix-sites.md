<properties
    pageTitle="deployment/visual studio or webmatrix"
    description="部署/Visual Studio 或 WebMatrix"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32542216"
    resourceTags=""
    productPesIds="14748,16170"
    cloudEnvironments="public"
/>


# Visual Studio 或 Webmatrix 部署

## **建议的步骤**
若要解决通过 Web 部署进行 Visual Studio 部署时遇到的最常见问题，请尝试以下一种或多种方法：

1.  确保根据所用 Visual Studio 版本安装最新版本的 Azure SDK：[下载位置](https://azure.microsoft.com/downloads)。 <br>
2.  如果使用部署凭据，请确保： <br>
    a. 帐户未在 Azure Active Directory 中禁用。 <br>
    b. 用户帐户格式正确（用户帐户的前面不能有 Web 应用名称，也不能有 $）。 <br>
    c. 密码正确。 <br>
有关详细信息，请参阅：[有关部署凭据的 Wiki 文章](https://github.com/projectkudu/kudu/wiki/Deployment-credentials) <br>
3.  如果使用发布凭据，请确保： <br>
    a. 下载最新的发布配置文件，并且用户名的前面带有 $。 有关详细信息，请查看：[部署凭据 Wiki 文章](https://github.com/projectkudu/kudu/wiki/Deployment-credentials)。<br>
4.  默认情况下，在部署到 Azure 应用服务 Web 应用时，会尝试连接到 Web 应用的 SCM 站点 (http://<yourWebAppName>.scm.azurewebsites.net)。 请确保 Visual Studio 能够连接到该站点。 <br>
5.  如果应用在代理的后面，请确保 Visual Studio 经过正确的配置，可以使用代理服务器。 有关详细信息，请参阅：[有关“需要代理授权”错误的详细信息](https://msdn.microsoft.com/library/dn771556.aspx)

## **建议的文档**
[如何使用 Visual Studio 和 Web 部署来创建和部署一个简单的 ASP.NET MVC Web 项目](https://azure.microsoft.com/documentation/articles/web-sites-dotnet-get-started/)<br>
[使用 Visual Studio 进行 ASP.NET Web 部署 - 由 12 个部分组成的系列教程，介绍部署任务的整个范围](http://www.asp.net/mvc/overview/deployment/visual-studio-web-deployment/introduction)<br>
[使用 Team Foundation Server/Services 构建和部署 Azure Web Apps](https://blogs.msdn.microsoft.com/tfssetup/2016/04/01/build-and-deploy-azure-web-apps-using-team-foundation-serverservices-vnext-builds/)<br>
[如何使用 Visual Studio 部署 Azure Web 作业。](https://azure.microsoft.com/documentation/articles/websites-dotnet-deploy-webjobs/)<br>
[将包含成员资格、OAuth 和 SQL 数据库的安全 ASP.NET MVC 5 应用部署到 Web Apps。](https://azure.microsoft.com/documentation/articles/web-sites-dotnet-deploy-aspnet-mvc-app-membership-oauth-sql-database/)<br>
[排查 Web 部署问题](http://www.iis.net/learn/publish/troubleshooting-web-deploy)<br>
[通过 Web 管理服务 (WMSVC) 在远程 IIS 管理器连接上将 Web 部署工具（Web 部署）用作受委派用户时收到错误消息](https://support.microsoft.com/kb/2023855)



<!--HONumber=Oct16_HO3-->



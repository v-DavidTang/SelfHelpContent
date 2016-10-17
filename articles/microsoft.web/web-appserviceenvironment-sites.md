<properties
    pageTitle="app service environment"
    description="App Service 环境"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32542253"
    resourceTags=""
    productPesIds="14748"
    cloudEnvironments="public"
/>


# App Service 环境
## **建议的步骤**
<b>在应用服务环境 (ASE) 中，为何即使有 2 个可用的辅助角色，也只能创建一个应用服务计划 (ASP)？</b><br>
为了提供容错能力，应用服务环境 (ASE) 要求针对每个辅助角色池至少分配一个额外的计算资源。<br>
请查看以下文章了解详细信息：[配置 ASE - 容错注意事项](https://azure.microsoft.com/documentation/articles/app-service-web-configure-an-app-service-environment/)

<b>创建 ASE 超时</b><br>
创建应用服务环境 (ASE) 有时失败，同时活动日志中出现以下错误：<br>
 
    ResourceID: /subscriptions/{SubscriptionID}/resourceGroups/Default-Networking/providers/Microsoft.Web/hostingEnvironments/{ASEname}
    Error:{"error":{"code":"ResourceDeploymentFailure","message":"The resource provision operation did not complete within the allowed timeout period."}}


确保不存在以下任何情况：<br>
    1.子网太小 <br>
    2.子网非空 <br>
    3.ExpressRoute 不允许 ASE 的网络连接要求 <br>
    4.错误的网络安全组 (NSG) 不允许 ASE 的网络连接要求 <br>
    5.已启用强制隧道 <br>

有关详细信息，请查看： <br>
[如何创建应用服务环境](https://azure.microsoft.com/documentation/articles/app-service-web-how-to-create-an-app-service-environment/#Overview) <br>
[部署（创建）新 Azure 应用服务环境 (ASE) 时的最常见问题](https://blogs.msdn.microsoft.com/waws/2016/05/13/most-frequent-issues-when-deploying-creating-a-new-azure-app-service-environment-ase/)

## **建议的文档**
[什么是 App Service 环境？](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-intro/)<br>
[创建 App Service 环境？](https://azure.microsoft.com/documentation/articles/app-service-web-how-to-create-an-app-service-environment/)<br>
[在 App Service 环境中创建应用](https://azure.microsoft.com/documentation/articles/app-service-web-how-to-create-a-web-app-in-an-ase/)<br>
[配置 App Service 环境](https://azure.microsoft.com/documentation/articles/app-service-web-configure-an-app-service-environment/)<br>
[在 App Service 环境中缩放应用](https://azure.microsoft.com/documentation/articles/app-service-web-scale-a-web-app-in-an-app-service-environment/)<br>
[网络安全和体系结构](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-network-architecture-overview/)<br>
[设置地理分散的应用布局](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-geo-distributed-scale/)<br>
[实施分层的安全体系结构](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-layered-security/)<br>
[为 App Service 环境配置 Web 应用程序防火墙](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-web-application-firewall/)<br>
[在 App Service 环境中使用自动缩放](https://azure.microsoft.com/documentation/articles/app-service-environment-auto-scale/)<br>
[保护入站流量](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-control-inbound-traffic/)<br>
[连接到后端资源](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-securely-connecting-to-backend-resources/)<br>
[ExpressRoute 和 App Service 环境](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-network-configuration-expressroute/)<br>
[App Service 环境的自定义配置设置](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-custom-settings/)



<!--HONumber=Oct16_HO1-->



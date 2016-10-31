<properties
    pageTitle="microsoft azure web apps (azurewebsites.net) configuration"
    description="Microsoft Azure Web Apps (azurewebsites.net) 配置"
    service="microsoft.network"
    resource="trafficmanagerprofiles"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32336442"
    resourceTags=""
    productPesIds="15400"
    cloudEnvironments="public"
/>


# Microsoft Azure Web Apps (azurewebsites.net) 配置
## **建议的步骤**
仅“标准”SKU 或更高版 SKU 的 Web 应用可与流量管理器配合使用。 将无法通过调用流量管理器来添加更低版 SKU 的 Web 应用。 降级现有 Web 应用的 SKU 将导致流量管理器不再向该 Web 应用发送流量，并可能从流量管理器删除终结点。
有关详细信息，请查看[流量管理器终结点](https://azure.microsoft.com/documentation/articles/traffic-manager-endpoint-types/)。

## **建议的文档**
[使用流量管理器控制 Azure Web 应用](https://azure.microsoft.com/documentation/articles/web-sites-traffic-manager/)<br>





<!--HONumber=Oct16_HO3-->



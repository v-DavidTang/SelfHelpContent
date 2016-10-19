<properties
    pageTitle="I need to increase the number of Network Security rules in my NSG"
    description="如何增加 NSG 中的网络安全规则数目"
    service="microsoft.network"
    resource="networksecuritygroups"
    authors="radwiv"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 如何增加 NSG 中的网络安全规则数目。

## **建议的步骤**
NSG 规则数目的默认限制为 200。 通过提出支持票证可将此数目最多提高到 400（经典）或 500 (Azure Resource Manager)。 如果需要增加 NSG 中的安全规则数目，请遵循下面的步骤。<br>

1. 新建支持请求<br>
[新建支持请求](data-blade:Microsoft_Azure_Support.NewSupportRequestBlade)
2. 为“问题类型”选择“配额”。<br>
3. 为“配额类型”选择“网络: 经典”（或“网络: ARM”），然后在详细信息部分中输入 NSG 的详细信息。<br>

## **建议的文档**

[网络限制](https://azure.microsoft.com/documentation/articles/azure-subscription-service-limits/#networking-limits)<br>
[排查在 Azure 中新建虚拟机时遇到的部署问题](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)


<!--HONumber=Oct16_HO2-->



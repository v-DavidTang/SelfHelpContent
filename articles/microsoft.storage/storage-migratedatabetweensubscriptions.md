<properties
    pageTitle="Move Data Between Subscriptions"
    description="在订阅之间移动数据"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="passaree"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32551652"
    resourceTags=""
    productPesIds="15629"
    cloudEnvironments="public"
/>


# <a name="move-resources-between-rg-or-subscription"></a>在 RG 或订阅之间移动资源

## <a name="call-support-when-you-need-to"></a>有以下需要时，请致电支持人员**
- 将资源移到新的 Azure 帐户（和 [Active Directory 租户](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move)）。
- 移动经典资源时遇到[限制](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)方面的问题。

## <a name="move-resources-between-rg-or-subscription"></a>在 RG 或订阅之间移动资源**
- 移动 Resource Manager 资源。
- 根据[经典部署限制](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)移动经典资源

移动资源之前需执行的一些重要步骤。 验证这些条件可以避免错误。

1. 该服务必须支持移动资源的功能。 请参阅以下列表，了解[哪些服务支持移动资源](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move)。
2. 源订阅与目标订阅必须在同一个 [Active Directory 租户](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#services-that-enable-move)中。 若要移到新租户，请致电支持人员。
3. 必须针对要移动的资源的资源提供程序注册目标订阅。 否则会出现一条错误，指出未针对资源类型注册订阅。 将资源移到新的订阅时，可能会遇到此问题，但该订阅从未配合该资源类型使用。 若要了解如何检查注册状态和注册资源提供程序，请参阅 [Resource providers and types](https://azure.microsoft.com/documentation/articles/resource-manager-supported-services/#resource-providers-and-types)（资源提供程序和类型）。
4. 如果要移动 App Service 应用，请查看[应用服务限制](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#app-service-limitations)。
5. 如果要移动与恢复服务关联的资源，请查看[恢复服务限制](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#recovery-services-limitations)。
6. 如果要移动通过经典模型部署的资源，请查看[经典部署限制](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)。

## <a name="recommended-documents"></a>**建议的文档**
[将资源移到新资源组或订阅中](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/)




<!--HONumber=Nov16_HO2-->



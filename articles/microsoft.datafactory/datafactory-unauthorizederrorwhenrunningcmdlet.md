<properties 
    pageTitle="Unauthorized error when running a cmdlet" 
    description="运行 cmdlet 时收到未授权错误消息。" 
    service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="7"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>


# 运行 cmdlet 时发生未授权错误

## **建议的步骤**
你可能未在 Azure PowerShell 中使用正确的 Azure 帐户或订阅。 使用以下 cmdlet 选择要在 Azure PowerShell 中使用的正确 Azure 帐户和订阅。 

1. **Login-AzureRmAccount** - 使用正确的用户 ID 和密码。
2. **Get-AzureRmSubscription** - 查看帐户的所有订阅。 
3. **Select-AzureRmSubscription <subscription name>** - 选择正确的订阅。 使用在 Azure 门户中创建数据工厂时所用的同一个订阅。


<!--HONumber=Jul16_HO1-->



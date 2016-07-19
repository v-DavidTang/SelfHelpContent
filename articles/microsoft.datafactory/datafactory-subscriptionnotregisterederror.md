<properties 
    pageTitle="Error: The subscription is not registered to use namespace Microsoft.DataFactory" 
    description="收到错误：该订阅未注册为使用命名空间 Microsoft.DataFactory" 
    service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="1"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>


# 错误: 该订阅未注册为使用命名空间 'Microsoft.DataFactory'

## **建议的步骤**
出现此错误表示未在你的计算机上注册 Azure 数据工厂资源提供程序。 请执行以下操作： 

1. 启动 Azure PowerShell。 
2. 使用以下命令登录到你的 Azure 帐户：**Login-AzureRmAccount** 
3. 运行以下命令以注册 Azure 数据工厂提供程序：**Register-AzureRmResourceProvider -ProviderNamespace Microsoft.DataFactory**




<!--HONumber=Jul16_HO1-->



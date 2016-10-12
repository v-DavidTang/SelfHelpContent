<properties 
    pageTitle="Errors deploying a service" 
    description="部署服务时出错 " 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="public"   
/>
 

# 部署服务时出错 

## **建议的步骤**
1. 大多数部署失败的原因是服务启动时发生异常。 这可能是因为缺少依赖项或构造函数有异常，或者某个 Service Fabric 启动方法（RunAsync、OnActivateAsync、CreateServiceReplicaListeners、CreateServiceInstanceListeners）有异常。 请参阅“应用程序/服务的常见失败和故障排除步骤”部分，了解如何进行故障排除。
2. 确认实例/副本计数未超出群集大小。




<!--HONumber=Sep16_HO4-->



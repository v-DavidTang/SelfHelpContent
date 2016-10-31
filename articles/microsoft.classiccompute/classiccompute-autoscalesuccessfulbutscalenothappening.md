<properties 
    pageTitle="Autoscale seems to be successful but scaling is not happening"
    description="自动缩放似乎成功，但并没有发生缩放"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="jluk"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""  
    productPesIds=""
    cloudEnvironments="public"
/>


# 自动缩放似乎成功，但并没有发生缩放
下面是针对为何无法缩放提供的一套解决方案和解释。 <br>

## **建议的步骤**
* 确保所有角色实例处于**“就绪”**状态。 <br>
仅当所有角色都处于就绪状态时才能自动缩放。 <br>
* 尝试手动缩放。<br>
如果手动缩放成功，则可能表示自动缩放配置文件配置不当。 有多个自动缩放配置文件会影响自动缩放行为。 [创建和管理自动缩放配置文件] (https://azure.microsoft.com/documentation/articles/insights-autoscale-best-practices/#autoscale-concepts) 应该通过同一个门户完成，因为每个门户具有独特的默认自动缩放配置文件。 <br>
* 尝试以较小的增量缩放，因为部署应用程序的群集可能没有足够的可用内核。 <br>
* [联系 Microsoft] (data-blade:Microsoft_Azure_Support.NewSupportRequestBlade) 提高订阅配额限制，因为在没有足够计算配额的情况下，自动缩放无法成功。 <br>
* 创建具有最大所需实例数的主机服务，然后重新部署到其中。 以后可根据需要缩减该服务。 <br>
使用最大实例数进行部署可确保群集提供所需的容量。 <br>

## **建议的文档**
[关于自动缩放最佳实践] (https://azure.microsoft.com/documentation/articles/insights-autoscale-best-practices/#autoscale-best-practices) <br>
[关于云服务分配失败](https://azure.microsoft.com/documentation/articles/cloud-services-allocation-failures/) <br>



<!--HONumber=Oct16_HO2-->



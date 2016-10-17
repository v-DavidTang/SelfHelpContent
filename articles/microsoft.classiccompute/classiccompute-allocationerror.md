<properties 
    pageTitle="My deployment fails with allocation errors"
    description="部署失败并出现分配错误"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="jluk"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""  
    productPesIds=""
    cloudEnvironments="public"
/>


# 部署失败并出现分配错误

## **建议的步骤**
云服务部署（过渡或生产）可能已固定到单个群集。 当群集达到其容量限制时，部署将会失败。 请尝试以下步骤。

1. 等待一段时间，然后重试部署操作。<br>
等待一段时间后，群集上的资源可能会释放，使部署或缩放请求能够成功。   
2. 将包部署到新的云服务。<br>
部署到新的云服务往往可以在容量足够的新群集上继续部署。 如果成功，请更新 DNS，使其指向新的云服务。 
3. 删除生产和过渡槽，然后重新部署到现有云服务。<br>
新部署将转到具有足够容量的群集。 但是，在新部署准备就绪之前，这会导致停机。 
4. 删除地缘组并 [迁移到区域虚拟网络] (https://azure.microsoft.com/documentation/articles/virtual-networks-migrate-to-regional-vnet/)
 
## **建议的文档**
[关于云服务分配失败](https://azure.microsoft.com/documentation/articles/cloud-services-allocation-failures/) <br>
[关于常规分配失败](https://azure.microsoft.com/blog/allocation-failure-and-remediation/)


<!--HONumber=Oct16_HO1-->



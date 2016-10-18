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

## **建议的步骤**
1. 确保所有角色实例处于**“就绪”**状态。 <br>
2. 尝试手动缩放。 <br>
3. 检查可用核心数。 <br>
如果订阅达到了最大计算核心数，可以 [联系 Microsoft ] 提高订阅计算配额限制 (data-blade:Microsoft_Azure_Support.NewSupportRequestBlade)。
4. 当部署到的群集达到容量限制或者没有所请求的计算核心类型时，可能会发生这种情况。 <br>
    * 尝试以较小的增量缩放。 <br>
    * 创建具有最大所需实例数的新主机服务，然后重新部署到其中。 完成初始部署后，可按需缩减。 使用最大实例数进行部署可确保群集提供所需的容量。 <br>

## **建议的文档**
[关于云服务分配失败](https://azure.microsoft.com/documentation/articles/cloud-services-allocation-failures/) <br>



<!--HONumber=Oct16_HO1-->



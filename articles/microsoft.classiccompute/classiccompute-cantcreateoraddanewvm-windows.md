<properties    
    pageTitle="我无法创建或添加新的 VM"
    description="我无法创建或添加新的 VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="windows"
    productPesIds=""
    cloudEnvironments="public" 
 />
    
# 我无法创建或添加新的 VM
    
## **建议的步骤**
若要解决常见问题，请尝试下面的一种或多种方法。

1. 查看[审核日志](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter)以确定失败原因
2. 根据错误代码查找建议的操作 <br>
[根据有关创建或添加新 VM 的错误代码进行排除故障](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)
3. 尝试使用较小的 VM 或不同的云服务来执行请求。 如果使用不同的云服务，请参考以下文章。 <br>
[Configure regional Virtual Network to connect Cloud services（配置区域虚拟网络以连接云服务）](https://azure.microsoft.com/blog/vnet-to-vnet-connecting-virtual-networks-in-azure-across-different-regions/)
4. 如果要使用自定义映像来创建新 VM，请参阅以下文章，以验证你在创建映像时是否遵循了必要的步骤[Capture an image of an Azure Windows virtual machine created with the classic deployment model](https://azure.microsoft.com/documentation/articles/virtual-machines-capture-image-windows-server/)（捕获使用经典部署模型创建的 Azure Windows 虚拟机的映像）

## **建议的文档**
[Troubleshooting allocation failure when you create, restart or resize a VM in Azure（在 Azure 中创建、重新启动 VM 或调整其大小时排查分配失败问题）](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/)

<!--HONumber=Jun16_HO1-->



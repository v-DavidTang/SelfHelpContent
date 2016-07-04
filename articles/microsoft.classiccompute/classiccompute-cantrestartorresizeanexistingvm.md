<properties    
    pageTitle="I can't restart or resize an existing VM"
    description="我无法重新启动现有 VM 或调整其大小 "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="windows, linux"   
    productPesIds=""
    cloudEnvironments="public" 
 />
    

# 我无法重新启动现有 VM 或调整其大小

## **建议的步骤**
若要解决常见问题，请尝试下面的一种或多种方法。

1. 查看[审核日志](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter)以确定失败原因
2. 根据错误代码查找建议的操作 <br>
[根据有关调整大小和重新启动的错误代码进行故障排除](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)
3. 尝试使用较小的 VM 或不同的云服务来执行请求。 如果使用不同的云服务，请参考以下文章。 <br>
[Configure regional Virtual Network to connect Cloud services（配置区域虚拟网络以连接云服务）](https://azure.microsoft.com/blog/vnet-to-vnet-connecting-virtual-networks-in-azure-across-different-regions/)

## **建议的文档**
[Troubleshooting allocation failure when you create, restart or resize a VM in Azure（在 Azure 中创建、重新启动 VM 或调整其大小时排查分配失败问题）](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/)



<!--HONumber=Jun16_HO5-->



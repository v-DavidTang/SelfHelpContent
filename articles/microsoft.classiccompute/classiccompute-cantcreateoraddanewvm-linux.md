<properties 
    pageTitle="I can't create or add a new VM" 
    description="我无法创建或添加新的 VM " 
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds="32411817,32449676"
    resourceTags="linux"
    productPesIds="14749"
    cloudEnvironments="public" 
 />
    

# 我无法创建或添加新的 VM

## **建议的步骤**
1. 查看[审核日志](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter)以确定失败原因
2. 根据错误代码查找建议的操作 <br>
[根据有关创建或添加新 VM 的错误代码进行排除故障](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)
3. 尝试使用较小的 VM 或不同的云服务来执行请求。 如果使用不同的云服务，请参考以下文章。 <br>
[Configure regional Virtual Network to connect Cloud services（配置区域虚拟网络以连接云服务）](https://azure.microsoft.com/blog/vnet-to-vnet-connecting-virtual-networks-in-azure-across-different-regions/)
4. 如果要使用自定义映像来创建新 VM，请参阅以下文章，以验证你在创建映像时是否遵循了必要的步骤 <br>
[How to capture a classic Linux virtual machine as an image（如何捕获用作映像的经典 Linux 虚拟机）](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-capture-image/)

## **建议的文档**
[Troubleshooting allocation failure when you create, restart or resize a VM in Azure（在 Azure 中创建、重新启动 VM 或调整其大小时排查分配失败问题）](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/)



<!--HONumber=Jul16_HO2-->



<properties
    pageTitle="Troubleshoot latency issues"
    description="排查延迟问题"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="passaree"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32551664"
    resourceTags=""
    productPesIds="15629"
    cloudEnvironments="public"
/>


# 排查延迟问题

## **建议的步骤**
诊断和排查云环境中托管的分布式应用程序的延迟问题可能很复杂。 下面描述了指标可能会变高的一些常见延迟情况，以及如何排查这些问题。 

你是否建立了基准指标？ 应用程序的性能可能是主观判定的，尤其是从用户角度来看，更是如此。 因此，请务必设置可用于帮助你确定是否可能存在性能问题的基准指标。 

1. [指标显示 AverageE2ELatency 较高且 AverageServerLatency 较低](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-high-AverageE2ELatency-and-low-AverageServerLatency)
2. [指标显示 AverageE2ELatency 和 AverageServerLatency 都较低，但客户端出现高延迟](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-low-AverageE2ELatency-and-low-AverageServerLatency)
3. [指标显示 AverageServerLatency 较高](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-high-AverageServerLatency)
4. [队列中的消息传递出现意外延迟](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#you-are-experiencing-unexpected-delays-in-message-delivery)

有关排查性能问题的深入探讨，请参阅 [**Monitor, diagnose, and troubleshoot Microsoft Azure Storage**](http://go.microsoft.com/fwlink/?LinkId=785091)（监视、诊断和排查 Microsoft Azure 存储空间问题）一文中的“Performance”（性能）部分

## **建议的文档**
[如何排查存储性能问题？](http://go.microsoft.com/fwlink/?LinkId=785091)



<!--HONumber=Oct16_HO3-->



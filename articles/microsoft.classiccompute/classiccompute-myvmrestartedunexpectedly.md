<properties 
    pageTitle="My VM restarted unexpectedly"
    description="我的 VM 意外重新启动 "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="8"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="windows, linux"   
    productPesIds=""
    cloudEnvironments="public" 
/>
    

# 我的 VM 意外重新启动

## **建议的步骤**
重新启动 VM 的常见原因如下：Azure 引起的问题（计划内或计划外的维护或服务中断），或者操作系统或应用程序的问题。 执行以下步骤可以找出过去重新启动的原因，并避免将来再次发生重新启动。

1. 查看重新启动时间段内的[审核日志](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter)以确定原因
2. 使用“可用性集”来降低停机事件造成的影响 <br>
[管理虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability/)

## **建议的文档**
[Planned maintenance for Azure virtual machines（Azure 虚拟机的计划内维护）](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/) <br>
[View and analyze Azure Audit Logs in Power BI and more（在 Power BI 和其他组件中查看和分析 Azure 审核日志）](https://azure.microsoft.com/blog/analyze-azure-audit-logs-in-powerbi-more/) 


<!--HONumber=Jun16_HO5-->



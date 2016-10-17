<properties 
    pageTitle="When using Autoscale, I get error 'Metrics data not available'"
    description="使用自动缩放时出现错误“指标数据不可用”"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="jluk"
    displayOrder="8"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""  
    productPesIds=""
    cloudEnvironments="public"
/>


# 使用自动缩放时出现错误“指标数据不可用”
自动缩放要求监视角色实例中的数据，这样才能缩放。 数据收集偶尔会出现延迟。 当自动缩放无法获取指标数据时，会缩放为**默认值**（如果该值高于当前实例计数）。 当自动缩放开始接收指标数据时，此问题会自行解决。 <br>
## **建议的步骤**
1. 如果这种情况导致生产出现问题，请关闭自动缩放，并手动缩放为所需的实例数。
2. 将缩放 **TimeWindow**（持续时间）设置为 30 分钟或以上。

## **建议的文档**
[关于缺少监视数据] (https://social.msdn.microsoft.com/Forums/azure/bc2048c4-8d49-4c54-b150-f263808c4b7a/notification-could-not-automatically-scale-xxx-because-monitoring-data-was-not-found?forum=windowsazuremanagement) <br>


<!--HONumber=Oct16_HO1-->



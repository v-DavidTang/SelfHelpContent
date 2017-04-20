<properties
    pageTitle="What metrics can I use to autoscale my scale set"
    description="可以使用哪些指标来自动缩放规模集"
    service="microsoft.compute"
    resource="virtualmachinescalesets"
    authors="gatneil"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>


# <a name="what-metrics-can-i-use-to-autoscale-my-scale-set"></a>可以使用哪些指标来自动缩放规模集

Azure 中为 VM 和规模集提供两种指标：主机指标和来宾指标。 主机指标来自 VM 主机，来宾指标来自来宾 OS。 所有 VM 自动发出主机指标，但若要查看来宾指标，需要将 Windows 诊断扩展或 Linux 诊断扩展添加到 VM/规模集。

## <a name="recommended-documents"></a>建议的文档

有关详细信息，请参阅[此文档](https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-autoscale-common-metrics)，其中介绍了常用的指标。


<properties
    pageTitle="VMA RCA"
    description="RCA - 节点服务修复 - 节点崩溃"
    infoBubbleText="已找到 RCA"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ScottAzure"
    displayOrder=""
    articleId="UnexpectedVMReboot_33668E95-C74E-42EE-82F6-AFD3ACCC30BD"
    diagnosticScenario="UnexpectedVMReboot"
    selfHelpType="rca"
    supportTopicIds="32411816"
    resourceTags="windows, linux"
    productPesIds="14749"
    cloudEnvironments="public"
/>


#<a name="we-ran-diagnostics-on-your-resource-and-found-an-issue"></a>我们对你的资源运行了诊断并发现了问题

<!--issueDescription-->
## <a name="microsoft-azure-vm-availability-incident-diagnostic-information-for-vmname--vmname--"></a>**[vmname] 的 Microsoft Azure VM 可用性事件诊断信息<!--($vmname)-->** ##

Microsoft Azure 已结束我们对订阅 **[SubscriptionId]**<!--($SubscriptionId)--> 中你的虚拟机 (VM) **[vmname]**<!--($vmname)--> 的调查。 我们发现，你的 VM **在 [开始时间]<!--($StartTime)--> (UTC) 变得不可用**，在 **[结束时间]<!--($EndTime)--> (UTC) 恢复了可用性**。 这一**意外事件**是由于 **Azure 启动的临时 VM 关闭所致**。
<!--/issueDescription-->

该临时 VM 关闭由 Azure 监视系统触发，这些系统检测到运行 VM 的物理主机节点与 VHD 所在的 Azure 存储服务之间存在失败的 IO 事务。 按照设计，此操作已执行以保持 VM 的数据完整性。 节点检测到情况已好转之后，VM 便重新启动了。 在此时间内，与 VM 的 RDP 连接或对该 VM 内运行的任何其他服务的请求可能已失败。   

*若要确保在 Azure 中为应用程序提供高可用性，建议你将两个或更多虚拟机组合到一个可用性集中。此配置将确保提供更高级别的保护，并且在发生计划内或计划外维护事件期间提供冗余。可在以下文章中找到有关管理和配置虚拟机可用性的详细信息：*

* [管理虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)
* [配置虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)

Microsoft Azure 还通过 Azure 资源运行状况提供对 Azure 门户中的资源运行状况信息的访问，Azure 资源运行状况是一项服务，用于显示各个 Azure 资源的运行状况，并为排查问题提供可行的指南。 若要了解有关 Azure 资源运行状况的详细信息，请参阅以下文章：[了解和使用资源运行状况中心，以便将来排查这种情况](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

对于这可能给你带来的任何不便，我们深表歉意。 我们一直致力于改进该平台，以减少由于平台问题而导致的虚拟机可用性事件。

此致，Microsoft Azure 团队


<properties
    pageTitle="VMA RCA"
    description="RCA - 客户启动 - VM 内关闭"
    infoBubbleText="发现最近已重新启动。 请参阅右侧的详细信息。"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jozender"
    displayOrder=""
    articleId="UnexpectedVMReboot_F891E098-FCD0-4F60-BA1E-0CDB5A5C42B8"
    diagnosticScenario="UnexpectedVMReboot"
    selfHelpType="rca"
    supportTopicIds="32411816"
    resourceTags="windows, linux"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# <a name="we-ran-diagnostics-on-your-resource-and-found-an-issue"></a>我们对你的资源运行了诊断并发现了问题

<!--issueDescription-->
## <a name="vm-availability-incident-diagnostic-information-for---vmname--virtual-machine--vmname--"></a>**<!--$vmname-->虚拟机<!--/$vmname-->的 VM 可用性事件诊断信息：** ##
 
我们发现，你的 VM 在 **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** 变得不可用。 这一预期事件由**用户启动的关闭操作**所致。
<!--/issueDescription-->

此关闭由授权用户或进程从虚拟机中触发。 因此，你的 VM 已关闭并且保持此状态，直到执行了用户操作来重新启动它。    

Microsoft Azure 还可让你在 Azure 门户中访问资源运行状况和故障排除信息。<br>
若要了解有关 Azure 资源运行状况的详细信息，请参阅以下文章：<br>
* [了解资源运行状况中心并使用它来排查此方案将来出现的问题](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

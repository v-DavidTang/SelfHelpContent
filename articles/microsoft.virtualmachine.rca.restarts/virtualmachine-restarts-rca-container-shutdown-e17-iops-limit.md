<properties
    pageTitle="VMA RCA"
    description="RCA - 容器关闭 - E17 IOPS 限制"
    infoBubbleText="发现最近已重新启动。 请参阅右侧的详细信息。"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jozender"
    displayOrder=""
    articleId="UnexpectedVMReboot_E17_IOPS_Limit"
    diagnosticScenario="UnexpectedVMReboot"
    selfHelpType="rca"
    supportTopicIds="32411816"
    resourceTags="windows, linux"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# <a name="we-ran-diagnostics-on-your-resource-and-found-an-issue"></a>我们对你的资源运行了诊断并发现了问题

<!--issueDescription-->
我们发现，你的 VM <!--$vmname-->虚拟机<!--/$vmname--> 在 **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** 变得不可用，在 **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)** 恢复了可用性。
发生这种意外问题的原因是在运行 VM 的物理主机节点与虚拟硬盘 (VHD) 所在的 Azure 存储服务之间检测到**临时 IO 事务超时**，从而触发了 **Azure 启动的 VM 关闭**。
<!--/issueDescription-->

Azure 标准存储磁盘有每个 VHD 500 IOPS 的限制。  我们已记录了一些最佳做法，用于[配置 Azure 虚拟机以获得最佳存储性能](http://blogs.msdn.com/b/mast/archive/2014/10/14/configuring-azure-virtual-machines-for-optimal-storage-performance.aspx)<br> 根据工作负荷，使用带区磁盘或在来宾 VM 内配置存储空间将可能有助于减轻此问题。  如果问题仍然存在，还可能需要考虑使用高级存储。<br>
 
为了确保提高 Azure 中应用程序的保护和冗余级别，我们建议将两个或更多虚拟机组合到一个可用性集中。<br>
若要了解有关高可用性选项的详细信息，请参阅以下文章：<br>
* [管理虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [配置虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)
* [托管磁盘概述](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)<br>

Microsoft Azure 还可让你在 Azure 门户中访问资源运行状况和故障排除信息。<br>
若要了解有关 Azure 资源运行状况的详细信息，请参阅以下文章：<br>
* [了解资源运行状况中心并使用它来排查此方案将来出现的问题](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>

对于这可能给你带来的任何不便，我们深表歉意。 我们一直致力于改进该平台，以减少由于平台问题而导致的虚拟机可用性事件。


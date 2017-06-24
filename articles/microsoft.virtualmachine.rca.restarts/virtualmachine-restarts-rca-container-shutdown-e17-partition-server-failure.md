<properties
    pageTitle="VMA RCA"
    description="RCA - 容器关闭 - E17 分区服务器故障"
    infoBubbleText="发现最近已重新启动。 请参阅右侧的详细信息。"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jozender"
    displayOrder=""
    articleId="UnexpectedVMReboot_RCA-Container_shutdown-E17_Partition_Server_Failure"
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
发生这种意外问题的原因是在运行 VM 的物理主机节点与虚拟硬盘 (VHD) 所在的 Azure 存储服务之间检测到**临时 IO 事务超时**，从而触发了 **Azure 启动的 VM 关闭**。 负载均衡操作所花费的时间超过预期，因此发生了 IO 超时。 
<!--/issueDescription-->

Azure 平台会持续监视 VM 对 Azure 存储的读取和写入（IO 事务）。  如果事务速度太慢或者在 120 秒内无法完成（包括重试），则会将连接视为断开，同时启动临时 VM 关闭，以保持数据完整性并防止 VM 损坏。 平台检测到存储服务连接已还原后，VM 已自动重启。 在此时间内，与 VM 的 RDP 连接或对该 VM 内运行的任何其他服务的请求可能已失败。<br>

Azure 存储是一个多租户环境中，这意味单个存储群集要为多个存储帐户提供服务。  Azure 存储使用分区系统，该系统可根据流量自动对群集中多个服务器上的分区进行负载均衡。 负载均衡可识别到给定分区服务器存在资源受限的情况，并将一个或多个分区范围重新分配到利用程度不足的分区服务器。 完成此操作所花费的时间比一般情况下的预期时间要长。  完成此操作后，分区中的数据可用，并且 VM 已恢复可用性。<br>

有关负载均衡和分区服务器故障的详细信息，请参阅以下文档： <br>
* [Microsoft Azure 存储体系结构概述](https://blogs.msdn.microsoft.com/windowsazurestorage/2010/12/30/windows-azure-storage-architecture-overview/)<br>
 
有关如何设计分区命名约定以实现最佳负载均衡的详细信息，请参阅[“存储性能和可伸缩性清单”中的相关部分](https://docs.microsoft.com/en-us/azure/storage/storage-performance-checklist#subheading47)。<br>

为了确保提高 Azure 中应用程序的保护和冗余级别，我们建议将两个或更多虚拟机组合到一个可用性集中。<br>
若要了解有关高可用性选项的详细信息，请参阅以下文章：<br>
* [管理虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [配置虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)
* [托管磁盘概述](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)<br>

Microsoft Azure 还可让你在 Azure 门户中访问资源运行状况和故障排除信息。<br>
若要了解有关 Azure 资源运行状况的详细信息，请参阅以下文章：<br>
* [了解资源运行状况中心并使用它来排查此方案将来出现的问题](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>

对于这可能给你带来的任何不便，我们深表歉意。 我们一直致力于改进该平台，以减少由于平台问题而导致的虚拟机可用性事件。


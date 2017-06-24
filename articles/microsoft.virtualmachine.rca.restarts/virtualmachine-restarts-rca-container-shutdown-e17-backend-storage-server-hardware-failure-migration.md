<properties
    pageTitle="VMA RCA"
    description="RCA - 容器关闭 - E17 后端存储服务器硬件故障 - 迁移"
    infoBubbleText="发现最近已重新启动。 请参阅右侧的详细信息。"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jozender"
    displayOrder=""
    articleId="UnexpectedVMReboot_RCA-Container_shutdown-E17_Backend_Storage_Server_Hardware_Failure_Migration"
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
发生这种意外问题的原因是在运行 VM 的物理主机节点与虚拟硬盘 (VHD) 所在的 Azure 存储服务之间检测到**临时 IO 事务超时**，从而触发了 **Azure 启动的 VM 关闭**。 由于在迁移到不同后端存储服务器时发生硬件故障，并且花费的时间较长，因此发生了 IO 超时。
<!--/issueDescription-->

Azure 平台会持续监视 VM 对 Azure 存储的读取和写入（IO 事务）。  如果事务速度太慢或者在 120 秒内无法完成（包括重试），则会将连接视为断开，同时启动临时 VM 关闭，以保持数据完整性并防止 VM 损坏。 平台检测到存储服务连接已还原后，VM 已自动重启。 在此时间内，与 VM 的 RDP 连接或对该 VM 内运行的任何其他服务的请求可能已失败。<br>

受影响的 VM 在后端存储节点上包含发生了硬件故障的 VHD。 已自动检测到此故障，并且针对 VHD 的存储操作已重定向到正常的后端存储服务器。 执行这种自我修复操作所花费的时间导致处理存储请求出现延迟并且 VM 暂时不可用。 我们将不断努力改进自我修复功能，以尽量减少甚至消除系统中任何硬件故障所造成的影响。<br>

有关存储体系结构的一般信息以及连接断开具体原因的详细信息，请参阅以下文档中的“分区服务器故障”部分：<br>
* [Microsoft Azure 存储体系结构概述](https://blogs.msdn.microsoft.com/windowsazurestorage/2010/12/30/windows-azure-storage-architecture-overview/)<br>
 
为了确保在 Azure 中为应用程序提供高可用性，我们建议将两个或更多虚拟机组合在一个可用性集中，并使用托管磁盘。 若要了解有关高可用性选项的详细信息，请参阅以下文章：<br>
若要了解有关高可用性选项的详细信息，请参阅以下文章：<br>
* [管理虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [配置虚拟机的可用性](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)
* [托管磁盘概述](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview) <br>

Microsoft Azure 还可让你在 Azure 门户中访问资源运行状况和故障排除信息。<br>
若要了解有关 Azure 资源运行状况的详细信息，请参阅以下文章：<br>
* [了解资源运行状况中心并使用它来排查此方案将来出现的问题](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>

对于这可能给你带来的任何不便，我们深表歉意。 我们一直致力于改进该平台，以减少由于平台问题而导致的虚拟机可用性事件。


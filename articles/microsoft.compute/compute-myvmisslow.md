<properties 
    pageTitle="My VM is slow"
    description="我的 VM 运行速度很慢"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds="32411877"
    resourceTags="windows, linux, windowsSQL, redhat"     
    productPesIds="14749"
    cloudEnvironments="public"
/>


# <a name="my-vm-is-slow"></a>我的 VM 运行速度很慢

## <a name="recommended-steps"></a>**建议的步骤**
请尝试执行以下步骤来诊断和解决 VM 性能问题。

1. 查看你的应用程序错误日志、跟踪和度量值，以确定是否存在任何导致性能问题的应用程序级瓶颈 <br>
从一次性问题中恢复的快速方法是重新启动应用程序和虚拟机
2. 查看操作系统级别的度量值，如 CPU、内存使用量、IO 和网络，以确定是否有任何资源的利用率一贯较高 <br>
在 Windows 上，使用 Perfmon 工具。 在 Linux 上，使用 Top、VmStat、 Lsof 和 Tcpdump 等命令。
3. 在 Azure 门户中使用 VM 诊断和存储诊断来识别是否有任何资源被过度使用或受到限制 <br>
[启用诊断，监视、识别并解决 Azure VM 和存储的问题](http://aka.ms/azurevmperf)
4. 通过[重新部署](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy) VM（将其迁移到新的 Azure 主机）来解决任何 Azure 主机问题。
5. 在 VM 资源的“设置”边栏选项卡中单击“大小”，将虚拟机扩展到其他 VM 类型或系列以提高性能
6. 如果该虚拟机用于 I/O 密集型方案，请考虑使用高级存储帐户 <br>
[高级存储：适用于 Azure 虚拟机工作负荷的高性能存储](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/)
7. 你是否知道，PerfInsights 可以帮助你分析来宾 VM 问题？ 请从这里开始：[下载 PerfInsights](https://www.microsoft.com/en-us/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True)。<br> 为确保快速解决问题，你还可以在创建支持案例时向我们提供 PerfInsights 日志。

## <a name="recommended-documents"></a>**建议的文档**
[Detailed troubleshooting of Azure Storage](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/)（Azure 存储的详细疑难解答）


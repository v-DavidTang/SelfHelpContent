<properties
    pageTitle="worker role (paas)/configuration and management/scaling and managing"
    description="辅助角色 (paas) /配置和管理/缩放和管理"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="ChiragPavecha"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32553317"
    resourceTags=""
    productPesIds="13185"
    cloudEnvironments="public"
/>


# <a name="worker-role-paasapplication-and-service-availabilityscaling-and-managing"></a>辅助角色 (paas)/应用程序和服务可用性/缩放和管理

## <a name="recommended-steps"></a>**建议的步骤**
Azure 自动缩放要求监视角色实例中的数据，这样才能缩放。 数据收集偶尔会出现延迟。
当自动缩放[无法获取指标数据](https://social.msdn.microsoft.com/Forums/bc2048c4-8d49-4c54-b150-f263808c4b7a/notification-could-not-automatically-scale-xxx-because-monitoring-data-was-not-found?forum=windowsazuremanagement)时，将缩放到默认实例计数（如果该值高于当前实例计数）。
当自动缩放重新开始接收指标数据时，此问题会自行解决。 TimeWindow 的建议值为 30 分钟或更长时间。
有关详细信息，请参阅[自动缩放最佳做法](https://docs.microsoft.com/azure/best-practices-auto-scaling)。

其他要尝试的步骤：<br>

* 确保所有角色实例处于“就绪”状态。 仅当所有角色都处于“就绪”状态时才能自动缩放。<br>

* 尝试手动缩放。<br>
  如果手动缩放成功，则可能表示自动缩放配置文件配置不当。 有多个自动缩放配置文件会影响自动缩放行为。 建议从[新门户](https://portal.azure.com)创建和管理自动缩放配置文件。<br>
    
* 尝试以较小的增量缩放。<br> 如果部署了云服务的群集的资源不足，这样的缩放可能会成功。 缩放现有云服务时，计算资源只能从部署了你的服务的群集中分配。 有关详细信息，请参阅[排除分配故障](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures)。<br>

* 通过联系 Microsoft 提高订阅配额限制，因为在没有足够计算配额的情况下，自动缩放无法成功。<br>

* 创建主机服务，并使用所需的最大实例数重新部署到它，如果需要，则降低到较小的实例数。 使用最大实例数进行部署可确保群集提供所需的容量。<br>


## <a name="recommended-documents"></a>**建议的文档**
[如何缩放云服务？](https://azure.microsoft.com/documentation/articles/cloud-services-how-to-scale/) <br>
[无法缩放 25 个以上的实例？](https://azure.microsoft.com/documentation/articles/vs-azure-tools-debug-cloud-services-virtual-machines/#limitations-of-remote-debugging-in-azure)<br>
[有关“度量值数据不可用”的自动缩放通知](https://social.msdn.microsoft.com/Forums/bc2048c4-8d49-4c54-b150-f263808c4b7a/notification-could-not-automatically-scale-xxx-because-monitoring-data-was-not-found?forum=windowsazuremanagement)<br>

[如何管理（交换/删除部署、链接到资源）云服务？](https://azure.microsoft.com/documentation/articles/cloud-services-how-to-manage/) <br>
[如何在资源组之间移动云服务，有哪些限制？](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)
[如何为云服务角色配置 VM 大小](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs#configure-sizes-for-cloud-services)<br>
[如何更改现有云服务角色的 VM 大小](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs#changing-the-size-of-an-existing-role)


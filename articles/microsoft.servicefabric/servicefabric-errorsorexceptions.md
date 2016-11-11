<properties
    pageTitle="application/errors or exceptions"
    description="应用程序/错误或异常"
    service="microsoft.servicefabric"
    resource="clusters"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32449688"
    resourceTags=""
    productPesIds="15842"
    cloudEnvironments="public"
/>


# 应用程序/错误或异常

## **建议的步骤**

应用程序或服务的常见失败和故障排除步骤：

1.  在 Service Fabric Explorer 中查看有关失败的信息。 参阅“Service Fabric Explorer 中出现 System.XXX 错误”部分，确定哪个节点发生了故障。
2.  检查应用程序事件日志或 ETW 跟踪日志，了解引发的异常。
3.  确保异步方法（OpenAsync、CloseAsync、RunAsync）正确处理 CancellationToken，因为这涉及到 Service Fabric 是否会触发关闭副本操作。
4.  确保所有应用程序依赖项已包含在应用程序包中。
5.  常见的失败是入口点方法出现异常 - RunAsync、OnActivateAsync、CreateServiceReplicaListeners、CreateServiceInstanceListeners、OnCloseAsync、OnOpenAsync
6.  请将一个调试器连接到服务。

Service Fabric Explorer 中出现 System.XXX 错误时的有用提示：

+ System.FM 分区低于目标副本计数或实例计数：常见的原因是服务在启动时崩溃（因缺少依赖项或者 RunAsync 或 OnActivateAsync 崩溃）。  这种问题也有可能是因为某个组件（例如节点）重新启动或出现暂时性故障而临时造成的。
+ System.PLB ServiceReplicaUnplacedHealth：常见的原因是应用程序请求的副本计数超出了群集中可用的节点数。  这可能是因为应用程序清单配置不当，或者群集节点因缩减操作或意外的节点故障而不可用。
+ System.PLB MovementsDropped：常见的原因是 PLB 发出的移动请求被删除，重新启动分区副本可能会消除此问题
+ System.PLB NodeCapacityViolation：常见的原因是指标消耗量超出了节点容量，在群集中添加更多节点可能会消除此问题
+ System.PLB BalancingUnsuccessful：常见的原因是负载平衡器无法进一步平衡群集，确保 FD/UD 中具有同等数量的活动节点可能会消除此问题。
+ System.PLB UpgradePrimarySwapViolation：常见的原因是由于无法交换主服务器而导致升级处于停滞状态。 若要消除此问题，请确保节点上有足够的容量
+ System.PLB ConstraintFixUnsuccessful：常见的原因是负载平衡器无法进一步平衡群集，确保每个 FD/UD 中的每种节点类型具有同等数量的活动节点，并且这些节点上有足够的容量，可能会消除此问题。
+ System.PLB ServiceCorrelationError：常见的原因是服务相关性无法构成链，若要消除此问题，请删除服务，然后重新创建具有有效相关性的服务 
+ System.RAP ServiceOpenOperationDuration：常见的原因是应用程序的 RunAsync 方法中引发了异常。  请连接调试器、检查应用程序事件日志或 ETW 跟踪日志了解更多信息。


## **建议的文档**
1. 请参阅[在本地计算机开发设置中监视和诊断服务](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/)，了解如何在应用程序中配置 ETW 跟踪
2. 请参阅[使用 Visual Studio 调试 Service Fabric 应用程序](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/)，了解如何使用 Visual Studio 调试和查看远程 Service Fabric 应用的 ETW 跟踪
3. [排查常见问题](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-troubleshoot-common-scenarios/)<br>
4. [Reliable Actors 的诊断和性能监视](https://azure.microsoft.com/documentation/articles/service-fabric-reliable-actors-diagnostics/)<br>
5. [有状态 Reliable Services 的诊断功能](https://azure.microsoft.com/documentation/articles/service-fabric-reliable-services-diagnostics/)



<!--HONumber=Oct16_HO4-->



<properties 
    pageTitle="Service Fabric Explorer 中出现 System.XXX 错误" 
    description="Service Fabric Explorer 中出现 System.XXX 错误" 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="public,BlackForest,Fairfax"   
/>
    

# <a name="i-am-seeing-systemxxx-errors-in-service-fabric-explorer"></a>Service Fabric Explorer 中出现 System.XXX 错误 

## <a name="recommended-steps"></a>**建议的步骤**

+ System.FM 分区低于目标副本计数或实例计数：常见的原因是服务在启动时崩溃（因缺少依赖项或者 RunAsync 或 OnActivateAsync 崩溃）。  这种问题也有可能是因为某个组件（例如节点）重新启动或出现暂时性故障而临时造成的。
+ System.PLB ServiceReplicaUnplacedHealth：常见的原因是应用程序请求的副本计数超出了群集中可用的节点数。  这可能是因为应用程序清单配置不当，或者群集节点因缩减操作或意外的节点故障而不可用。
+ System.PLB MovementsDropped：常见的原因是 PLB 发出的移动请求被删除，重新启动分区副本可能会消除此问题
+ System.PLB NodeCapacityViolation：常见的原因是指标消耗量超出了节点容量，在群集中添加更多节点可能会消除此问题
+ System.PLB BalancingUnsuccessful：常见的原因是负载平衡器无法进一步平衡群集，确保 FD/UD 中具有同等数量的活动节点可能会消除此问题。
+ System.PLB UpgradePrimarySwapViolation：常见的原因是由于无法交换主服务器而导致升级处于停滞状态。 若要消除此问题，请确保节点上有足够的容量
+ System.PLB ConstraintFixUnsuccessful：常见的原因是负载平衡器无法进一步平衡群集，确保每个 FD/UD 中的每种节点类型具有同等数量的活动节点，并且这些节点上有足够的容量，可能会消除此问题。
+ System.PLB ServiceCorrelationError：常见的原因是服务相关性无法构成链，若要消除此问题，请删除服务，然后重新创建具有有效相关性的服务 
+ System.RAP ServiceOpenOperationDuration：常见的原因是应用程序的 RunAsync 方法中引发了异常。  请连接调试器、检查应用程序事件日志或 ETW 跟踪日志了解更多信息。

## <a name="recommended-documents"></a>**建议的文档**
1. 
          [使用系统运行状况报告进行故障排除](https://azure.microsoft.com/documentation/articles/service-fabric-understand-and-troubleshoot-with-system-health-reports/)中描述了大部分系统错误



<!--HONumber=Jan17_HO1-->



<properties 
    pageTitle="应用程序/服务的常见失败和故障排除步骤" 
    description="应用程序/服务的常见失败和故障排除步骤" 
    service="microsoft.ServiceFabric"
    resource="clusters"
    authors="pkcsf"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="public,BlackForest,Fairfax"   
/>
    

# <a name="common-failures-and-troubleshooting-steps-for-applicationservice"></a>应用程序/服务的常见失败和故障排除步骤

## <a name="recommended-steps"></a>**建议的步骤**
1.  在 Service Fabric Explorer 中查看有关失败的信息。 参阅“Service Fabric Explorer 中出现 System.XXX 错误”部分，确定哪个节点发生了故障。
2.  检查应用程序事件日志或 ETW 跟踪日志，了解引发的异常。
3.  确保异步方法（OpenAsync、CloseAsync、RunAsync）正确处理 CancellationToken，因为这涉及到 Service Fabric 是否会触发关闭副本操作。
4.  确保所有应用程序依赖项已包含在应用程序包中。
5.  常见的失败是入口点方法出现异常 - RunAsync、OnActivateAsync、CreateServiceReplicaListeners、CreateServiceInstanceListeners、OnCloseAsync、OnOpenAsync
6.  请将一个调试器连接到服务。
  
## <a name="recommended-documents"></a>**建议的文档**
1.  请参阅[在本地计算机开发设置中监视和诊断服务](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/)，了解如何在应用程序中配置 ETW 跟踪
2.  请参阅[使用 Visual Studio 调试 Service Fabric 应用程序](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/)，了解如何使用 Visual Studio 调试和查看远程 Service Fabric 应用的 ETW 跟踪


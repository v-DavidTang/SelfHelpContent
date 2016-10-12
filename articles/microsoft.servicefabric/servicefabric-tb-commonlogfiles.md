<properties 
    pageTitle="Common log files for Service Fabric nodes" 
    description="Service Fabric 节点的常见日志文件" 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="public"   
/>
    

# Service Fabric 节点的常见日志文件

## **建议的步骤**
只需使用一条命令，就能轻松地从 Service Fabric 节点中捕获所有最常见的日志文件。  这会创建一个 ZIP 文件，可将它离线保存供事后分析。  若要创建该 ZIP 文件，请通过 [RDP](https://azure.microsoft.com/documentation/articles/service-fabric-cluster-nodetypes/#remote-connect-to-a-vm-scale-set-instance-or-a-cluster-node) 连接到节点，然后运行 CollectGuestLogs.exe。  可以在 Azure 来宾代理文件夹 (C:\WindowsAzure\Packages\CollectGuestLogs.exe) 中找到 CollectGuestLogs.exe。 在收集的文件中，下面是排查问题时使用最多的文件：
 
 - 事件日志
   - Service Fabric 事件日志
   - 应用程序和系统事件日志
   - Azure 事件日志
 + Azure 来宾代理日志
 + 扩展/插件安装日志和状态 Blob
 + 节点配置
 + Service Fabric 安装日志
 + Windows Azure 诊断日志和缓存的数据

## **建议的文档**
1.  请参阅[在本地计算机开发设置中监视和诊断服务](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/)，了解如何在应用程序中配置 ETW 跟踪
2.  请参阅[使用 Visual Studio 调试 Service Fabric 应用程序](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/)，了解如何使用 Visual Studio 调试和查看远程 Service Fabric 应用的 ETW 跟踪




<!--HONumber=Sep16_HO4-->



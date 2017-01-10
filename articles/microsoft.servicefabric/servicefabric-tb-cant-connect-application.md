<properties 
    pageTitle="连接到群集中部署的应用程序失败 " 
    description="连接到群集中部署的应用程序失败 " 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    displayOrder="9"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="public,BlackForest,Fairfax"   
/>
 

# <a name="connection-failures-to-applications-deployed-in-a-cluster"></a>连接到群集中部署的应用程序失败 

## <a name="recommended-steps"></a>**建议的步骤**

1. 验证负载平衡规则是否将公开的公共端口映射到预期的内部端口和后端地址池 [查看“资源组”->“负载平衡器[LB xxx]”->“负载平衡规则”]。
2. 验证 ServiceManifest.xml 是否包含一个定义了正确协议和端口映射的终结点。 请参阅[在服务清单中指定资源](https://azure.microsoft.com/documentation/articles/service-fabric-service-manifest-resources/)。
3. 检查是否有网络安全组规则阻止了流量。在“网络设置”中，查看“资源组”->“虚拟网络”->“子网”->“安全组”。
4. 确保应用程序配置为侦听正确的端口。 为了实现此目的，通常可以在 CreateServiceInstanceListeners 方法中调用 CodePackageActivationContext.GetEndpoint 来获取服务清单中配置的终结点。
5. 对于 HTTP 终结点，请通过 RDP 连接到运行该应用程序的节点之一，然后在命令提示符下执行：netsh http show servicestate view=requestq：这样就会显示已注册到 http.sys 的所有服务的进程 ID 和已注册 URL。
6. 通过 RDP 连接到运行该应用程序的节点之一，然后使用网络跟踪工具（Netmon、Message Analyzer、Wireshark 等）监视传入的流量。  这可以帮助确定流量是否进入群集，或者客户端与 Azure Load Balancer 之间的某个位置是否出现问题。
7. 从不同的客户端进行测试以消除客户端网络问题，尤其是当客户端位于企业网络环境，特定的端口或流量被阻止时。  最好是从另一台 Azure VM 进行测试，消除 Azure 外部可能存在的任何网络问题。



<!--HONumber=Jan17_HO1-->



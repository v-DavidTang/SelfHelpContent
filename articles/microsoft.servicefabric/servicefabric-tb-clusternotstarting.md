<properties 
    pageTitle="群集未启动或节点未显示" 
    description="群集未启动或节点未显示" 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="public,BlackForest,Fairfax"   
/>
    

# <a name="my-cluster-is-not-starting-or-nodes-are-not-displaying"></a>群集未启动或节点未显示

## <a name="recommended-steps"></a>**建议的步骤**
1. 请查看[审核日志](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter)，检查 ARM 部署或资源分配是否失败
2. 查看“网络设置”，确保 NSG 设置允许将传入流量发往端口 19080 [“资源组”->“虚拟网络”->“子网”->“安全组”]
3. 通过 [RDP](https://azure.microsoft.com/documentation/articles/service-fabric-cluster-nodetypes/#remote-connect-to-a-vm-scale-set-instance-or-a-cluster-node) 连接到某个节点，然后在应用程序事件日志和 Microsoft-Service-Fabric 管理事件日志中查看错误。  SFAdmin 日志中可能会出现几个暂时性警告条目，可以将其忽略。 应查看其描述与群集设置失败相关的错误条目。 有关日志文件的详细信息，请参阅“Service Fabric 节点的常见日志文件”部分


<properties
    pageTitle="configurationandsetup/troubleshootconnectivity"
    description="configurationandsetup/troubleshootconnectivity"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32584260"
    resourceTags=""
    productPesIds="15526"
    cloudEnvironments="public"
/>


# configurationandsetup/troubleshootconnectivity
<a id="configurationandsetuptroubleshootconnectivity" class="xliff"></a>

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>
1. 使用 [IP 流验证](data-blade:microsoft_azure_network.verifyipflowblade)检查是允许还是拒绝了传入或传出 VM 的流量<br>
2. 使用[安全组视图](data-blade:microsoft_azure_network.networkwatchersecuritygroupviewblade)查看 NIC 上的关联 NSG 和规则，以及 VM 的子网级别<br>
3. 使用路由的[下一跃点](data-blade:microsoft_azure_network.getnexthopblade)查找来自特定 VM 和 NIC 的数据包的下一跃点类型和 IP 地址<br>
4. 使用 [NSG 流日志](data-blade:microsoft_azure_network.flowlogsblade)查看通过网络安全组的入口和出口 IP 流量<br>
5. 使用[数据包捕获](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade)跟踪传入和传出 VM 的流量<br>

## **建议的文档**
<a id="recommended-documents" class="xliff"></a>
[网络观察程序概述](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview)<br>
[了解 Azure 中的出站连接](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)

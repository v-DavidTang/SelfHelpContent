<properties
    pageTitle="connectivity/othernetworkconnectivityproblems"
    description="connectivity/othernetworkconnectivityproblems"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32547255"
    resourceTags=""
    productPesIds="15526"
    cloudEnvironments="public"
/>


# <a name="connectivityothernetworkconnectivityproblems"></a>connectivity/othernetworkconnectivityproblems

## <a name="recommended-steps"></a>**建议的步骤**
1. 使用 [IP 流验证](data-blade:microsoft_azure_network.verifyipflowblade)检查是否允许传入或传出虚拟机的流量<br>
2. 使用路由的[下一跃点](data-blade:microsoft_azure_network.getnexthopblade)查找来自特定 VM 和 NIC 的数据包的下一跃点类型和 IP 地址<br>

## <a name="recommended-documents"></a>**建议的文档**
[网络观察程序概述](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview)<br>
[了解 Azure 中的出站连接](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)<br>
[辅助 NIC 无法连接到网络](https://docs.microsoft.com/azure/virtual-network/virtual-networks-multiple-nics#secondary-nics-access-to-other-subnets)<br>
[使用静态 IP 创建 VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-deploy-static-pip-arm-portal)<br>
[将现有 IP 设为静态](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-addresses#a-namechange-ip-configachange-ip-address-settings)<br>
[将多个 IP 添加到 VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-multiple-ip-addresses-portal)<br>


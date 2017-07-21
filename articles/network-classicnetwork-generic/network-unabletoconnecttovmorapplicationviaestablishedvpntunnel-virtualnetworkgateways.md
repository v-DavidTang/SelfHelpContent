<properties
    pageTitle="unable to connect to vm or application via established vpn tunnel"
    description="无法通过建立的 VPN 隧道连接到 VM 或应用程序"
    service="microsoft.network"
    resource="virtualnetworkgateways"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32542249"
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="public"
/>


# <a name="unable-to-connect-to-vm-or-application-via-established-vpn-tunnel"></a>无法通过建立的 VPN 隧道连接到 VM 或应用程序

## <a name="recommended-steps"></a>**建议的步骤**
1. 检查 VPN 连接的资源运行状况
2. 使用 [VPN 诊断](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade)排查本地连接问题
3. 查看 VPN 日志（在存储帐户中提供）以查找 VPN 隧道或设备配置的任何问题
4. 使用[数据包捕获](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade)跟踪传入和传出 VM 的流量
5. 使用 [IP 流验证](data-blade:microsoft_azure_network.verifyipflowblade)检查是否允许传入或传出虚拟机的流量

## <a name="recommended-documents"></a>**建议的文档**
查看[已验证的 VPN 设备](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides)列表，确保设备已配置并且兼容<br>
参阅 [IKE 参数](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-nameipsecaipsecike-parameters)以确定设备的隧道设置<br>
[使用网络观察程序诊断通过 VPN 网关的本地连接](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity)<br>
使用[在 VPN 连接上执行的 IP 流验证](https://docs.microsoft.com/azure/network-watcher/network-watcher-check-ip-flow-verify-portal)检查流量<br>
使用 [Azure 网络观察程序](https://azure.microsoft.com/services/network-watcher/)深入了解 Azure 网络



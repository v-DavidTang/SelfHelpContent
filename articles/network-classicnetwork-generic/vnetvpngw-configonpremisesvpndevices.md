<properties
    pageTitle="configure on-premises vpn devices"
    description="配置本地 VPN 设备"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds=" 32584874"
    resourceTags=""
    productPesIds="15526"
    cloudEnvironments="public"
/>


# <a name="configure-on-premises-vpn-devices"></a>配置本地 VPN 设备

## <a name="recommended-steps"></a>**建议的步骤**

1. 使用 [VPN 诊断](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade)排查本地连接问题
2. 查看 VPN 日志（在存储帐户中提供）以查找 VPN 隧道或设备配置的任何问题

## <a name="recommended-documents"></a>**建议的文档**
查看[已验证的 VPN 设备](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides)列表，确保设备已配置并且兼容<br>
参阅 [IKE 参数](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-nameipsecaipsecike-parameters)以确定设备的隧道设置<br>
检查 Azure [第三方设备配置](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-3rdparty-device-config-overview)以了解设备是否可用<br>
有关 Cisco ASA 配置示例，请参阅[将基于路由的 IKEv2 与 CISCO ASA 配合使用](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-3rdparty-device-config-cisco-asa)<br>
诊断[通过 VPN 网关的本地 VPN 连接问题](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity)


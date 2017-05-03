<properties
    pageTitle="ADFS & SharePoint connections fail behind Load Balancer over VPN"
    description="在负载均衡器后面通过 VPN 进行ADFS 和 SharePoint 连接时失败"
    service="microsoft.network"
    resource="loadbalancers"
    authors="radwiv"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="adfs--sharepoint-connections-fail-behind-load-balancer-over-vpn"></a>在负载均衡器后面通过 VPN 进行ADFS 和 SharePoint 连接时失败

## <a name="recommended-steps"></a>**建议的步骤**
1.    将 ADFS 服务器的最大传输单元 (MTU) 调整到 1350 而不是依赖于路径 MTU 发现 (PMTUD)，因为内部负载均衡器 (ILB) 不支持 PMTUD 传递。
2.    使用第三方网络设备进行负载均衡（在 Azure 门户中可用）。
3.    使用外部负载均衡器 (ELB/ SLB) 而不使用 ILB 将此流量移出 VPN，从而不会达到 MTU 限制。


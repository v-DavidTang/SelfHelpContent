<properties
    pageTitle="VMs behind Load Balancer (LB) not responding to requests"
    description="负载均衡器 (LB) 后面的 VM 未响应请求"
    service="microsoft.network"
    resource="loadbalancers"
    authors="radwiv"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="vms-behind-load-balancer-lb-not-responding-to-requests"></a>负载均衡器 (LB) 后面的 VM 未响应请求

## <a name="recommended-steps"></a>**建议的步骤**

1.    若要了解如何对第三方网络设备进行故障排除和配置，请联系该设备的供应商。
2.    为外部 LB 启用 [LB 诊断](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log)，以确定 Azure 平台是否在检测问题。
3.    检查门户中的 LB 运行状况探测设置。 如果它是为 HTTP 配置的，请将其更改为 TCP，然后测试并记录结果。
4.    远程连接到 LB 后面的 VM，然后运行命令 "netstat -an" (Windows) 或 "netstat -l" (Linux)。<br>
    如果无法看到结果中列出的探测信息和数据 TCP 端口，可能需要配置 VM 上的应用程序以侦听和响应探测信息和数据端口。
5.    在 VNet（不在 LB 后面）中，使用[Psping](https://technet.microsoft.com/sysinternals/psping.aspx)（适用于 Windows）或 nmap（适用于 Linux），测试探测信息和数据端口响应（示例：psping 10.0.0.4:80 或 nmap-p 80 10.0.0.4）。 如果未收到响应，请进行检查以确保 NSG/UDR 未被阻止。
6.    运行 PsPing 或 nmap 时，请在 LB VM 和 VNet 测试 VM 上运行同步网络跟踪，然后停止跟踪。<br>
    a.在“解决方案资源管理器”中，右键单击项目文件夹下的“引用”文件夹，然后单击“添加引用”。 对于 Windows，运行："netsh trace start capture=yes tracefile=c:\server_IP.etl scenario=netconnection"，对于 Linux，运行："sudo tcpdump -s0 -i eth0 -X -w vmtrace.cap" <br>
    b. 从 VNet VM 到 LB VM，使用 psping 或 nmap（示例：psping 10.0.0.4:80 或 nmap -p 80 10.0.0.4）<br>
    c. 使用网络监视器 (Windows) 或 tcpdump (Linux) 从后端 VM 打开网络跟踪，并对运行了 PsPing 或 nmap 的 VM 的 IP 应用显示筛选器，例如 "IPv4.address==10.0.0.4"(Windows netmon) 或 "tcpdump -nn -r vmtrace.cap src or dst host 10.0.0.4" (Linux)<br>
    如果无法看到数据包传入到后端 VM 跟踪，那么很可能存在 NSG/UDR 干扰。 如果看到数据包传入但没有响应，则可能需要解决 VM 应用程序或防火墙问题。<br>
7.    内部负载均衡器 (ILB)：如果仅当从本地网络通过 VPN/ExpressRoute 进行测试时才发生此问题，而从 VNet 中的 VM 进行测试时不会再现此问题，请通过 VPN/ExpressRoute 测试从本地资源到 VNet 中其他非负载平衡 VM 的通信。 此问题可能与应检查的 VPN/ExpressRoute 连接相关。
8.    外部负载均衡器 (ELB/SLB)：如果仅当从本地网络到负载均衡器的公共 IP 地址进行测试时才发生此问题，而从另一个位置（例如家庭或咖啡店）进行测试时不会发生此问题，那么很可能是本地代理或防火墙设置有问题。
9.    外部负载均衡器 (ELB/SLB)：如果在 VNet 或 LB 子网上应用了 VPN/ExpressRoute 和[强制隧道](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)或[默认路由](https://github.com/Microsoft/azure-docs/blob/master/articles/expressroute/expressroute-routing.md#advertising-default-routes)，可能会破坏正常的通信路由。

## <a name="recommended-documents"></a>**建议的文档**
用于 Azure Load Balancer [LB 诊断](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log)的 Log Analytics<br>
配置[强制隧道](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)



<!--HONumber=Feb17_HO2-->



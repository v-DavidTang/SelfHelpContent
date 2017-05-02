<properties
    pageTitle="VMs behind Load Balancer (LB) not responding to requests"
    description="负载均衡器 (LB) 后面的 VM 未响应请求"
    service="microsoft.network"
    resource="loadbalancers"
    authors="radwiv"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="vms-behind-load-balancer-lb-not-responding-to-requests"></a>负载均衡器 (LB) 后面的 VM 未响应请求

## <a name="recommended-steps"></a>**建议的步骤**
1. 若要了解如何对第三方网络设备进行故障排除和配置，请联系设备供应商。 
2. 为外部 LB 启用 LB 诊断，确定 Azure 平台是否在检测问题。 
3. 检查负载均衡器后端池中的虚拟机是否响应负载均衡器探测<br>
    a. 检查虚拟机是否已启动并且可用。<br>
    b. 检查虚拟机是否正在侦听探测端口（使用命令“netstat-an”(Windows) 或“netstat-l”(Linux)）。<br>
    c. 检查负载均衡器后端池 VM 上的网络安全组是否允许探测端口上的流量（参阅[排查网络安全组问题](https://docs.microsoft.com/azure/virtual-network/virtual-network-nsg-troubleshoot-portal)）<br>
    d. 检查现行的用户定义路由是否干扰了探测数据包路由（参阅[排查路由问题](https://docs.microsoft.com/azure/virtual-network/virtual-network-routes-troubleshoot-portal)）<br>
    e. 如果为 HTTP 配置了负载均衡器运行状况探测，请将 HTTP 更改为 TCP，并验证 TCP 是否开始响应探测。<br> 
4. 检查负载均衡器后端池中的虚拟机是否正在接收并响应数据端口上的流量<br>
    a. 检查虚拟机是否正在侦听数据端口（使用命令“netstat-an”(Windows) 或“netstat-l”(Linux)）。<br>
    b. 检查负载均衡器后端池 VM 上的网络安全组是否允许数据端口上的流量（参阅[排查网络安全组问题](https://docs.microsoft.com/azure/virtual-network/virtual-network-nsg-troubleshoot-portal)）<br>
    c. 检查现行的用户定义路由是否干扰了数据包路由（参阅[排查路由问题](https://docs.microsoft.com/azure/virtual-network/virtual-network-routes-troubleshoot-portal)）<br>
    d. 检查后端池中的参与 VM 是否正在尝试访问内部负载均衡器 VIP。 此方案不受支持。<br>
5. 收集网络捕获以跟踪数据包流<br> 
    a. 在负载均衡器 VM 以及同一虚拟网络中的另一个测试 VM 上运行同步网络跟踪（对于 Windows，请运行：“netsh trace start capture=yes tracefile=c:\server_IP.etl scenario=netconnection”；对于 Linux，请运行：“sudo tcpdump -s0 -i eth0 -X -w vmtrace.cap”）<br>
    b. 在两个 VM 之间运行 PsPing 并捕获一些数据包交换数据。 停止跟踪。<br>
    c. 使用网络监视器 (Windows) 或 tcpdump (Linux) 从后端 VM 打开网络跟踪，并对运行了 PsPing 或 nmap 的 VM 的 IP 应用显示筛选器，例如 "IPv4.address==10.0.0.4"(Windows netmon) 或 "tcpdump -nn -r vmtrace.cap src or dst host 10.0.0.4" (Linux)<br>
   如果无法看到数据包传入到后端 VM 跟踪，原因很可能是存在 NSG/UDR 干扰。 如果看到数据包传入但没有响应，则可能需要解决 VM 应用程序或防火墙问题。<br>
6. 从组织本地通过 VPN/Express Route 建立连接出现问题<br>
    a. 测试从本地网络到虚拟网络中任一非负载均衡虚拟机的连接，确保 VPN/Express Route 连接正常。<br>
    b. 测试从本地网络和外部到公共 IP 地址的连接，确保本地防火墙未阻止流量。<br>
    c. 检查是否已配置强制隧道，或者在 VNet 或 LB 子网中应用了默认路由。 这可能会中断正常的路由。<br>

## <a name="recommended-documents"></a>**建议的文档**
[排查 Azure 负载均衡器问题](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot)<br>
用于 Azure 负载均衡器[LB 诊断](https://docs.microsoft.com/azure/load-balancer/load-balancer-monitor-log)的 Log Analytics<br>
配置[强制隧道](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)


<properties
    pageTitle="My Load Balanced VMs are not receiving traffic"
    description="负载均衡的 VM 不接收流量"
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


# <a name="my-load-balanced-vms-are-not-receiving-traffic"></a>负载均衡的 VM 不接收流量

## <a name="recommended-steps"></a>**建议的步骤**
如果在虚拟网络中配置了负载均衡器并出现连接问题，请尝试以下一个或多个步骤来解决该问题。<br>

1. 检查负载均衡器后端池中的虚拟机是否响应负载均衡器探测<br>
    a. 检查虚拟机是否已启动并且可用。<br>
    b. 检查虚拟机是否正在侦听探测端口。<br>
    c. 检查负载均衡器后端池 VM 上的网络安全组是否允许探测端口上的流量。<br>

2. 检查负载均衡器后端池中的虚拟机是否正在接收并响应数据端口上的流量<br>
    a. 检查虚拟机是否正在侦听数据端口。<br>
    b. 检查负载均衡器后端池 VM 上的网络安全组是否允许数据端口上的流量。<br>
    c. 检查后端池中的参与 VM 是否未尝试访问内部负载均衡器 VIP。<br>

## <a name="recommended-documents"></a>**建议的文档**
[排查 Azure 负载均衡器问题](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot)


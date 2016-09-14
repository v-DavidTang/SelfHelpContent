<properties
    pageTitle="I am unable to connect to virtual machines in the same VNet when using an UDR."
    description="排查使用 UDR 时同一 VNet 中出现的 VM 连接问题"
    service="microsoft.network"
    resource="routetables"
    authors="radwiv"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 使用 UDR 时无法连接到同一 VNet 中的虚拟机。

## **建议的步骤**
如果在虚拟网络子网中使用用户定义的路由并出现连接问题，请尝试下面一个或多个步骤来解决此问题。<br>

1. 检查路由条目，确保出现问题的目标地址已被一个或多个路由覆盖。 虚拟网络中与本地和 Internet 之间的通信已被系统路由涵盖。<br>
[用户定义的路由概述](https://azure.microsoft.com/documentation/articles/virtual-networks-udr-overview/)
2. 检查是否可从其他源访问目标。<br>
3. 检查源和目标上的网络安全组规则是否允许此流量。<br>
4. 如果使用 NVA 来路由流量，请检查 NVA VM 是否正在运行，以及是否启用了“IP 转发”。<br>
5. 验证 NVA 是否不在与源虚拟机相同的子网中。 否则会产生路由循环。<br>

## **建议的文档**

[用户定义的路由设计注意事项](https://azure.microsoft.com/documentation/articles/best-practices-network-security/#examples-building-security-boundaries-with-azure-virtual-networks)


<!--HONumber=Aug16_HO5-->



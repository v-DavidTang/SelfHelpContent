<properties
    pageTitle="I can't connect to services deployed in my VNet"
    description="无法连接到 VNet 中部署的服务"
    service="microsoft.network"
    resource="expressroutecircuits"
    authors="kasparks"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 无法连接到 VNet 中部署的服务

## **建议的步骤**
若要解决最常见问题，请尝试下面的一种或多种方法。

1. 检查是否已创建 VPN 网关。<br>
[检查是否为虚拟网络创建了 VPN 网关（类型 = ExpressRoute）](https://azure.microsoft.com/documentation/articles/expressroute-howto-add-gateway-resource-manager/)
2. 检查 VNet 与 ExpressRoute 线路之间的连接。<br>
检查是否在 VNet 与 ExpressRoute 线路之间建立了连接。 检查是否已启用连接。
3. 检查网络与 Microsoft 之间的第 3 层连接。
    1. 获取 Azure 专用对等互连的路由表摘要。
    2. 检查你的路由器与 Microsoft 路由器之间是否有活动的 BGP 会话。 你的网络与 Microsoft 之间必须有一对活动的 BGP 会话（一个主要会话，一个辅助会话）。
    3. 请联系你的服务提供商解决任何问题（如果路由是他们管理的）。
    4. 查看我们的路由器配置参考示例。
    5. 如果路由是你自己管理的，请检查是否设置了正确的参数。
        1. 检查 BGP 邻居 IP 地址。
        2. 检查你的 ASN（对等 ASN）和 Azure ASN (12076)。
        3. 如果你配置了 MD5 哈希（会话密钥），请检查哈希。
    6. 检查你的 VNet 之间是否有活动的 BGP 会话。 你（使用 AS65515）连接到的每个 VNet 必须有一对活动的 BGP 会话。 BGP 邻居 IP 是 VNet 的网关子网中的专用 IP 地址。
4. 检查与你的虚拟网络建立的第 3 层连接。
    1. 获取 Azure 专用对等互连的路由表摘要。
    2. 检查你的 VNet 之间是否有活动的 BGP 会话。 你（使用 AS65515）连接到的每个 VNet 必须有一对活动的 BGP 会话。 BGP 邻居 IP 是 VNet 的网关子网中的专用 IP 地址。
5. 检查是否播发了所有前缀。
    1. 获取 Azure 专用对等互连的路由表。
    2. 检查包含相应下一跃点的路由表中是否存在全部所需的前缀（在本地和虚拟网络中）。

## **建议的文档**
[有关更多详细信息，请参阅以下 ExpressRoute 疑难解答文档](https://azure.microsoft.com/documentation/services/expressroute/)



<!--HONumber=Jun16_HO5-->



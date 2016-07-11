<properties
    pageTitle="I can't connect to services offered through Azure Public peering"
    description="无法连接到通过 Azure 公共对等互连提供的服务"
    service="microsoft.network"
    resource="expressroutecircuits"
    authors="kasparks"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 无法连接到通过 Azure 公共对等互连提供的服务

## **建议的步骤**
若要解决最常见问题，请尝试下面的一种或多种方法。

1. 检查网络与 Microsoft 之间的第 3 层连接。
    1. 获取 Azure 公共对等互连的路由表摘要。
    2. 检查你的路由器与 Microsoft 路由器之间是否有活动的 BGP 会话。 你的网络与 Microsoft 之间必须有一对活动的 BGP 会话（一个主要会话，一个辅助会话）。
    3. 请联系你的服务提供商解决任何问题（如果路由是他们管理的）。
    4. 查看我们的路由器配置参考示例。
    5. 如果路由是你自己管理的，请检查是否设置了正确的参数
        1. 检查 BGP 邻居 IP 地址。
        2. 检查你的 ASN（对等 ASN）和 Azure ASN (12076)。
        3. 如果你配置了 MD5 哈希（会话密钥），请检查哈希。
2. 检查是否播发了所有前缀。
    1. 获取 Azure 公共对等互连的路由表。
    2. 检查包含相应下一跃点的路由表中是否存在全部所需的前缀。
3. 检查本地 NAT 配置。
    1. 在 Azure.com 上查看 NAT 示例
    2. 检查你的 NAT 配置。
4. 检查防火墙。 <br>
检查本地防火墙配置。
5. 检查路由。 <br>
检查本地网络中的路由，以确保正确传播路由。

## **建议的文档**
[有关更多详细信息，请参阅以下 ExpressRoute 疑难解答文档](https://azure.microsoft.com/documentation/services/expressroute/)



<!--HONumber=Jun16_HO5-->



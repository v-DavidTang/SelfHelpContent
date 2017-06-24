<properties
    pageTitle="vnetpeering/managevnetpeering"
    description="vnetpeering/managevnetpeering"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32547254"
    resourceTags=""
    productPesIds="15526"
    cloudEnvironments="public"
/>


# <a name="vnetpeeringmanagevnetpeering"></a>vnetpeering/managevnetpeering

## <a name="recommended-documents"></a>**建议的文档**
[VNet 对等互连概述](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview)
[如何创建、更改或删除 VNet 对等互连](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering) 

## <a name="frequently-asked-questions"></a>常见问题
### <a name="i-created-a-peering-why-am-i-not-able-to-ping-the-vm-in-the-peer-vnet"></a>**我已创建对等互连，但为何无法 ping 通对等 VNet 中的 VM？**
请确保对等互连的状态显示为“已连接”。 如果对等互连的状态为“已启动”，则表示只创建了一个链接。 因此，若要成功建立对等互连，需要建立两个对等链接。 请阅读[创建虚拟网络对等互连](https://docs.microsoft.com/azure/virtual-network/virtual-networks-create-vnetpeering-arm-portal)一文，查看有关如何执行此操作的分步教程。

### <a name="is-transitive-vnet-peering-possible"></a>**能否建立可传递 VNet 对等互连？**
VNet 对等互连存在于两个 VNet 之间，多个对等互连之间没有任何派生的可传递关系。 例如，如果 VNet A 与 VNet B 对等互连，VNet B 与 VNet C 对等互连，但 VNet A 不与 VNet C 对等互连。 若要在 VNet A 与 C 之间建立连接，必须在两者间建立对等互连。

### <a name="how-do-i-peer-across-subscriptions"></a>**如何跨订阅建立对等互连？**
若要跨订阅建立对等互连，需要对订阅拥有特定的权限。 [跨订阅对等互连](https://docs.microsoft.com/azure/virtual-network/virtual-networks-create-vnetpeering-arm-portal#a-namex-subapeering-across-subscriptions)一文介绍了相关操作。


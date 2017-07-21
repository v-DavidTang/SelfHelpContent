<properties
    pageTitle="configurationandsetup/howtoassociateansgwithavmorsubnet"
    description="configurationandsetup/howtoassociateansgwithavmorsubnet"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32584255"
    resourceTags=""
    productPesIds="15526"
    cloudEnvironments="public"
/>


# <a name="configurationandsetuphowtoassociateansgwithavmorsubnet"></a>configurationandsetup/howtoassociateansgwithavmorsubnet

## <a name="recommended-steps"></a>**建议的步骤**
1. 使用[安全组视图](data-blade:microsoft_azure_network.networkwatchersecuritygroupviewblade)查看 NIC 上的关联 NSG 和规则，以及 VM 的子网级别<br>
2. 使用路由的[下一跃点](data-blade:microsoft_azure_network.getnexthopblade)查找来自特定 VM 和 NIC 的数据包的下一跃点类型和 IP 地址<br>

## <a name="recommended-documents"></a>**建议的文档**
[将 NSG 关联到 VM、NIC 或子网](https://docs.microsoft.com/azure/virtual-network/virtual-networks-nsg#associating-nsgs)<br>
[创建 NSG](https://docs.microsoft.com/azure/virtual-network/virtual-networks-create-nsg-arm-pportal)
[以经典方式创建外围网络](https://docs.microsoft.com/azure/virtual-network/virtual-networks-dmz-nsg-asm)
[在 ARM 中创建 Azure 与 Internet 之间的外围网络](https://docs.microsoft.com/azure/architecture/reference-architectures/dmz/secure-vnet-dmz)


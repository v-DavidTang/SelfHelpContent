<properties
    pageTitle="ipaddresses/ipaddresschangedafterreboot"
    description="ipaddresses/ipaddresschangedafterreboot"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="viorican"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32547250"
    resourceTags=""
    productPesIds="15526"
    cloudEnvironments="public"
/>


# <a name="ipaddressesipaddresschangedafterreboot"></a>ipaddresses/ipaddresschangedafterreboot

## <a name="recommended-documents"></a>**建议的文档**
[IP 分配方法](https://azure.microsoft.com/documentation/articles/virtual-network-ip-addresses-overview-arm/#allocation-method)
[添加、更改或删除 IP 地址](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-network-interface-addresses)

## <a name="frequently-asked-questions"></a>常见问题
### <a name="why-are-there-missing-ip-addresses-in-my-vnet"></a>**VNet 中为何缺少 IP 地址？**
Azure 在每个子网中保留 5 个 IP 地址。 子网的第一个和最后一个 IP 地址仅为协议一致性而保留，其他 3 个地址用于 Azure 服务。

### <a name="why-cant-i-rdp-to-my-vm"></a>**为何无法通过 RDP 连接到 VM？**
若要通过 RDP 连接到 VM，需将一个公共 IP 关联到 VM。 若要了解如何关联或创建公共 IP，请阅读[创建公共 IP 地址](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address#a-namecreateacreate-a-public-ip-address)一文。


### <a name="the-ip-address-of-my-vm-changed-after-reboot-how-do-i-get-the-ip-address-back"></a>**重新启动后，VM 的 IP 地址已更改。如何恢复 IP 地址？**
很遗憾，丢失的 IP 地址无法恢复。 发生更改的原因是 IP 地址是动态的。 只有在将公共 IP 地址与附加到 VM 的 NIC 相关联并首次启动该 VM 时，才分配**动态**地址。 如果附加到 VM 的 NIC 已停止（解除分配），动态地址可能会更改。 **静态**地址是在创建公共 IP 地址时分配的。 即使 VM 处于停止（解除分配）状态，静态地址也不会发生更改。 仅当删除 NIC 时，才释放该地址。 创建 NIC 后，可以更改分配方法。 请阅读[创建具有静态公共 IP 地址的 VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-deploy-static-pip-arm-portal) 了解详细信息。


<properties
    pageTitle="management/cannotdeletevirtualnetwork"
    description="management/cannotdeletevirtualnetwork"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32584253"
    resourceTags=""
    productPesIds="15526"
    cloudEnvironments="public"
/>


# management/cannotdeletevirtualnetwork
<a id="managementcannotdeletevirtualnetwork" class="xliff"></a>

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>
1. 在[网络观察程序拓扑](data-blade:microsoft_azure_network.networkwatchertopologyblade)中检查连接到虚拟网络的设备<br>
2. 在删除虚拟网络之前，请务必先删除其中的所有设备。 正确的删除顺序是连接、网关、IP 和 VNet<br>

## **建议的文档**
<a id="recommended-documents" class="xliff"></a>
[删除虚拟网络网关](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-delete-vnet-gateway-portal)

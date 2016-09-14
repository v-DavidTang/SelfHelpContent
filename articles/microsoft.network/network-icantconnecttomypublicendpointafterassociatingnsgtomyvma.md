<properties
    pageTitle="I cannot connect to my public endpoint after associating NSG to my virtual machine"
    description="排查将 NSG 关联到 VM 后与公共终结点建立连接的问题"
    service="microsoft.network"
    resource="networksecuritygroups"
    authors="radwiv"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 将 NSG 关联到虚拟机后无法连接到公共终结点。

## **建议的步骤**
除非明确允许从 Internet 建立连接，否则 NSG 默认会拒绝这种连接。 若要解决此问题，请尝试下面一个或多个步骤。<br>

1. 查看 NSG 中的安全规则。<br>
2. 检查负载平衡器规则配置中使用的后端端口是否在允许列表中。<br>
3. 如果没有任何规则允许来自 Internet 的流量，请添加一个源为“Internet”、“*”或特定公共 IP 地址的新规则，允许访问后端端口。<br>

## **建议的文档**

[负载平衡器终结点的 NSG 规则](https://azure.microsoft.com/documentation/articles/virtual-networks-nsg/#load-balancers)<br>
[排查在 Azure 中新建虚拟机时遇到的部署问题](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)


<!--HONumber=Aug16_HO5-->



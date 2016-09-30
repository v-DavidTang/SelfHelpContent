<properties  
    pageTitle="I can't connect to an application on my VM"
    description="我无法连接到 VM 上的应用程序"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds="32411838"
    resourceTags="windows, linux, windowsSQL, redhat"    
    productPesIds="14749"
    cloudEnvironments="public"
/>
    

# 我无法连接到 VM 上的应用程序

## **建议的步骤**
首先，请确保能够通过 RDP 或 SSH 连接到 VM，然后尝试以下步骤。

1. 验证应用程序是否在侦听预期的端口和终结点 <br>
使用“netstat -a”显示 VM 上的活动侦听端口，然后检查终结点 ACL 规则中的公用和专用端口
2. 从不同的 VM 测试应用程序访问 <br>
尝试从同一虚拟网络中的不同虚拟机访问应用程序，然后从不同子网中的 VM 测试访问。 如果无法访问，请检查主机防火墙和[网络安全组配置](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade)。
3. 测试外部应用程序访问 <br>
尝试从虚拟网络外部的计算机访问该应用程序。 如果无法访问，请检查外部负载平衡器配置、终结点（TCP 或 UDP）、[网络安全组](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade)和 NAT 配置。

## **建议的文档**
[About network security groups（关于网络安全组）](https://azure.microsoft.com/documentation/articles/virtual-networks-nsg/) <br>
[Troubleshoot access to an application running on an azure virtual machine（对在 Azure 虚拟机上运行的应用程序的访问进行故障排除）](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-access-application/)



<!--HONumber=Sep16_HO4-->



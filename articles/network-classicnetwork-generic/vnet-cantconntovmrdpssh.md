<properties
    pageTitle="connectivity/cannotconnecttoavirtualmachineusingrdporssh"
    description="connectivity/cannotconnecttoavirtualmachineusingrdporssh"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32547225"
    resourceTags=""
    productPesIds="15526"
    cloudEnvironments="public"
/>


# connectivity/cannotconnecttoavirtualmachineusingrdporssh
<a id="connectivitycannotconnecttoavirtualmachineusingrdporssh" class="xliff"></a>

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>
遵循以下步骤解决网络相关的常见 RDP/SSH 问题：<br>
1. 使用 [IP 流验证](data-blade:microsoft_azure_network.verifyipflowblade)来确认网络安全组中的规则是否阻止了传入或传出虚拟机的流量。<br>
2. 检查生效的安全组规则，确保入站“允许”NSG 规则存在并已根据 RDP/SSH 端口（默认为 3389/22）设置优先级。<br>
3. 在启用强制隧道的情况下，可能无法使用 RDP/SSH 通过 Internet 连接到 VM。 使用强制隧道时，发往 Internet 的所有出站流量将重定向到本地。 检查生效的路由。<br>

## **建议的文档**
<a id="recommended-documents" class="xliff"></a>
[解决常见 RDP 连接问题的步骤](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)<br>
[解决常见 SSH 连接问题的步骤](https://docs.microsoft.com/azure/virtual-machines/linux/troubleshoot-ssh-connection)


<properties  
    pageTitle="I can't connect to my Windows VM"
    description="我无法连接到 Windows VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32411835"
    resourceTags="windows, windowsSQL"
    productPesIds="14749"
    cloudEnvironments="public"
/>


# <a name="i-cant-connect-to-my-windows-vm"></a>我无法连接到 Windows VM

###<a name="recommended-steps"></a>**建议的步骤**
若要解决常见问题，请尝试下面的一个或多个步骤。

1. 查看 VM 的[控制台屏幕截图](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade)以更正启动问题
2. 重置远程访问以解决远程服务器问题 <br>
[使用 PowerShell 或 CLI 重置远程访问](http://aka.ms/resetsarmwinremoteaccess)
3. 单击 VM 资源边栏选项卡顶部的“重新启动”来重新启动虚拟机，以解决启动问题
4. 使用 [IP 流验证](data-blade:microsoft_azure_network.verifyipflowblade)来确认网络安全组中的规则是否阻止了传入或传出虚拟机的流量。 还可以查看[有效的安全组规则](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade)，确保入站“允许”NSG 规则存在并已针对 RDP 端口（默认值 3389）进行优化。
5. 在启用强制隧道的情况下，可能无法使用 RDP 通过 Internet 连接到 VM。 请查看[有效的路由](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade)。 使用强制隧道时，发往 Internet 的所有出站流量将重定向到本地
6. 通过[重新部署](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy)（将 VM 迁移到新的 Azure 主机）来解决 Azure 主机问题
7. 如果你收到了 RDP 许可证错误，请使用“mstsc/admin”来解决错误。 如果需要，请卸载或购买 RDS 许可证。 <br>
[解决远程桌面许可证服务器错误](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#rdplicense)

###<a name="recommended-documents"></a>**建议的文档**
[排查特定的远程桌面连接错误](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#troubleshoot-specific-remote-desktop-connection-errors) <br>
[网络组件的详细故障排除步骤](https://azure.microsoft.com/documentation/articles/virtual-machines-rdp-detailed-troubleshoot/)


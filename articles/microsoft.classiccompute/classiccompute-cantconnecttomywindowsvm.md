
<properties 
    pageTitle="I can't connect to my Windows VM"
    description="我无法连接到 Windows VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32411835"
    resourceTags="windows, WindowsSQL"
    productPesIds="14749"
    cloudEnvironments="public"
 />
    

# 我无法连接到 Windows VM

## **建议的步骤**

可执行以下基本步骤来解决常见问题。

1. 查看 VM 的[控制台屏幕截图](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade)以更正启动问题
2. 单击 VM 资源边栏选项卡顶部的“重置远程访问”来重置远程桌面服务，以解决 RDP 服务器的启动问题
3. [重置密码](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade)以解决身份验证错误
4. 单击 VM 资源边栏选项卡顶部的“重新启动”来重新启动虚拟机，以解决其他启动问题
5. 在 VM 资源的“设置”边栏选项卡中单击“大小”来调整 VM 大小，以解决任何主机问题

## **建议的文档**
[Troubleshoot specific Remote Desktop connection errors（排查特定的远程桌面连接错误）](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#troubleshoot-specific-remote-desktop-connection-errors) <br>
[Detailed troubleshooting across network components（网络组件详细疑难解答）](https://azure.microsoft.com/documentation/articles/virtual-machines-rdp-detailed-troubleshoot/) <br>
[Address Remote Desktop License Server error（解决远程桌面许可证服务器错误）](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#rdplicense) 



<!--HONumber=Jul16_HO3-->



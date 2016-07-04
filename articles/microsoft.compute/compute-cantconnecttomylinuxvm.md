<properties 
    pageTitle="I can't connect to my Linux VM" 
    description="我无法连接到 Linux VM" 
    service="microsoft.compute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="linux"    
    productPesIds=""
    cloudEnvironments="public" 
/>
    

# 我无法连接到 Linux VM
 
## **建议的步骤**
 若要解决常见问题，请尝试下面的一个或多个步骤。
 
 1. 查看 VM 的[控制台屏幕截图或日志](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade)以更正启动问题。 查看 FSTAB（文件系统表）、FSCK （文件系统一致性）或网络等日志中的错误
 2. 重置密码以解决身份验证错误 <br>
 [使用 CLI 或 PowerShell 重置密码](http://aka.ms/resetarmpass)
 3. 单击 VM 资源边栏选项卡顶部的“重新启动”来重新启动虚拟机，以解决启动问题
 4. 通过[重新部署](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy)（将 VM 迁移到新的 Azure 主机）来解决任何 Azure 主机问题
 5. 重置 SSH 连接和配置以解决 SSH 问题 <br>
 [使用 CLI 或 PowerShell 重置 SSH 连接](http://aka.ms/resetarmssh)
 
## **建议的文档**
[Detailed troubleshooting of SSH errors（针对 SSH 错误的详细疑难解答）](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension（使用 CustomScript 扩展自动执行 Linux VM 自定义任务）](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)


<!--HONumber=Jun16_HO5-->



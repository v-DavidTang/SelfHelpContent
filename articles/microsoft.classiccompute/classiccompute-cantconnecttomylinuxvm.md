<properties 
    pageTitle="我无法连接到 Linux VM"
    description="我无法连接到 Linux VM "
    service="microsoft.classiccompute"
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
若要解决常见问题，请尝试下面的一种或多种方法。

1. 查看 VM 的[控制台日志或屏幕截图](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade)以更正启动问题。 查看 FSTAB（文件系统表）、FSCK （文件系统一致性）或网络等日志中的错误。
2. [重置密码](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade)以解决身份验证错误
3. 单击 VM 资源边栏选项卡顶部的“重新启动”来重新启动虚拟机，以解决启动问题
4. 在 VM 资源的“设置”边栏选项卡中单击“大小”来调整 VM 大小，以解决主机问题
5. 重置 SSH 配置以解决任何 SSH 问题 <br>
[使用 CLI 重置 SSH](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-use-vmaccess-reset-password-or-ssh/#sshconfigresetcli)

## **建议的文档**
[Detailed troubleshooting of SSH errors（针对 SSH 错误的详细疑难解答）](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension（使用 CustomScript 扩展自动执行 Linux VM 自定义任务）](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)

<!--HONumber=Jun16_HO1-->



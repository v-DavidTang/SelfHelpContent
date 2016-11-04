<properties
    pageTitle="Site Recovery (VMware to Azure)/Add vCenter"
    description="Site Recovery（VMware 到 Azure）/添加 vCenter 期间出现的常见问题"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="AnoopVasudavan"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536386"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# Site Recovery（VMware 到 Azure）/添加 vCenter

添加 vCenter 期间出现的常见问题

## **建议的步骤**

* 确保已在 **CSPSConfigtool.exe** 中添加一个帐户，以便连接到 **VMware vCenter**。

* 确保用于连接 vCenter 的帐户满足以下要求 [vCenter 帐户先决条件](http://aka.ms/vCenterAccountPrereq)。 执行以下步骤，检查该帐户是否有足够的权限
 - 以管理员身份启动 VMWare PowerCLI
 - 使用在 **CSPSConfigtool.exe** 中提供的相同**用户名**和**密码**连接到 vCenter
 - 使用 Get-VM 命令枚举所有虚拟机
 - 如果枚举了所有虚拟机，则该帐户适合由 Azure Site Recovery 用来发现虚拟机。

* 确保已在配置服务器/扩展进程服务器上安装 **VMware PowerCLI 6.0**。
 - 不支持更高/更低的 PowerCLI 版本。
 - 可以从 https://developercenter.vmware.com/tool/vsphere_powercli/6.0 下载 PowerCLI 6.0

* 确保每个虚拟机的虚拟硬盘 (VMDK) 存储独立的子目录中。 该目录应与虚拟机**同名**。


## **建议的文档**
[VMware 到 Azure](https://aka.ms/asrstv2a)



<!--HONumber=Oct16_HO3-->



<properties
    pageTitle="Site Recovery (VMM to Azure)/Not able to conect to VM after failover"
    description="Site Recovery（VMM 到 Azure）/故障转移后无法连接到 VM"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="prateek9us"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536424"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# Site Recovery（VMM 到 Azure）/故障转移后无法连接到 VM

## **无法连接到/无法通过 RDP/SSH 连接到故障转移的虚拟机**

### **虚拟机上的“连接”按钮灰显** 
* 如果部署模型为“Resource Manager” <br/>
在虚拟机的网络接口上添加一个公共 IP。 [请参阅此处所述的添加公共 IP 步骤](https://aka.ms/asr-resourcemanager-vm-connect)


* 如果部署模型为“经典” <br/>
在公共端口 3389（适用于 RDP）和公共端口 22（适用于 SSH）上添加一个终结点。 [请参阅此处所述的添加终结点步骤](https://aka.ms/asr-classic-vm-connect)

### **虚拟机上的“连接”按钮可用**
* 在虚拟机菜单中转到**“启动诊断”**，查看虚拟机的控制台屏幕截图。  默认情况下，已在 Resource Manager 虚拟机上启用了“启动诊断”。 在经典虚拟机上，需要手动启用它。 
    * 请注意，启用除“启动诊断”以外的任何设置，都需要在故障转移之前在虚拟机中安装 Azure VM 代理

* 如果虚拟机尚未启动，请尝试故障转移到以前的恢复点

* 如果虚拟机中的应用程序未启动，请尝试故障转移到应用一致的恢复点

* 如果虚拟机已加入域，请确保域控制器正常运行。 为此，可在同一网络中创建新虚拟机，并确保该虚拟机能够加入到预期要启动故障转移虚拟机的同一个域

    * 如果域控制器未正常运行，请尝试使用本地管理员帐户登录到故障转移的虚拟机
    
    
* 如果使用自定义 DNS 服务器，请确保可以访问该服务器。 为此，可在同一网络中创建新虚拟机，然后使用该自定义 DNS 服务器来检查该虚拟机是否能够执行名称解析


## **建议的文档**
[详细故障转移文档](https://azure.microsoft.com/documentation/articles/site-recovery-failover/)

[排查 RDP 连接问题](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-troubleshoot-rdp-connection/)



<!--HONumber=Oct16_HO3-->



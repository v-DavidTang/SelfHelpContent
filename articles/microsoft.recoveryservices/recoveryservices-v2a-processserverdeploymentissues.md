<properties
    pageTitle="Site Recovery (VMware to Azure)/Process Server deployment issues"
    description="Site Recovery（VMware 到 Azure）/在进程服务器部署期间出现的常见问题"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="AnoopVasudavan"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536429"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# <a name="site-recovery-vmware-to-azure-process-server-deployment-and-issues"></a>Site Recovery（VMware 到 Azure）/进程服务器部署和问题。

在进程服务器部署期间出现的常见问题

## <a name="recommended-steps"></a>**建议的步骤**
* 确保进程服务器部署到要保护/重新保护的虚拟机所在的同一网络中。
* 如果要在 Azure 中部署进程服务器，请确保为进程服务器选择正确的部署模型。 Resource Manager 虚拟机不能由经典模型进程服务器重新保护，反之亦然。
* 如果要在 Azure 中部署进程服务器，请确保在继续将其用于重新保护虚拟机之前，[将其注册到配置服务器](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-setup-azure-ps-resource-manager#registering-the-process-server-running-in-azure-to-a-configuration-server-running-on-premises)。

## <a name="recommended-documents"></a>**建议的文档**
* [在 Azure 中部署进程服务器 (Resource Manager) 以进行故障回复](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-setup-azure-ps-resource-manager)
* [在 Azure 中部署进程服务器（经典）以进行故障回复](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-setup-azure-ps-classic)
* [部署本地横向扩展进程服务器](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-scaleout-process-server)
* [将进程服务器（在 Azure 中运行）注册到配置服务器](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-setup-azure-ps-resource-manager#registering-the-process-server-running-in-azure-to-a-configuration-server-running-on-premises)
* [将横向扩展进程服务器（在本地运行）重新注册到配置服务器](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-scaleout-process-server#re-registering-a-scale-out-process-server)
* [对横向扩展进程服务器解除授权](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-scaleout-process-server#decommissioning-a-scale-out-process-server)
* [注销已断开连接的进程服务器](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-scaleout-process-server#unregistering-a-disconnected-scale-out-process-server-from-a-configuration-server)



<!--HONumber=Feb17_HO4-->



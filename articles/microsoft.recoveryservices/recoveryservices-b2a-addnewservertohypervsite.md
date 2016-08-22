<properties
    pageTitle="Site Recovery (Hyper-V Site to Azure)/Add new servers to Hyper-V site"
    description="站点恢复（Hyper-V 站点到 Azure）/将新服务器添加到 Hyper-V 站点"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="anoopkv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536385"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# 站点恢复（Hyper-V 站点到 Azure）/将新服务器添加到 Hyper-V 站点

将服务器添加到 Hyper-V 站点时出现的常见问题

## **建议的步骤**

* 确保安装 **Microsoft Azure Site Recovery 提供程序**的服务器有权访问以下 URL <br>
    1. *.hypervrecoverymanager.windowsazure.com
    2. *.accesscontrol.windows.net
    3. *.backup.windowsazure.com
    4. *.blob.core.windows.net
    5. *.store.core.windows.net

* 确保安装 **Microsoft Azure Site Recovery 提供程序**的服务器上的时钟已根据其目标时区设置了正确的时间。

* 如果你知道要安装 **Microsoft Azure Site Recovery 提供程序**的服务器在代理服务器后面，请始终选择“使用代理服务器连接到 Azure Site Recovery”选项。

* 不应在域控制器上安装 **Microsoft Azure Site Recovery 提供程序**


## **建议的文档**
[本地先决条件](https://azure.microsoft.com/documentation/articles/site-recovery-hyper-v-site-to-azure/#on-premises-prerequisites)



<!--HONumber=Aug16_HO3-->



<properties
    pageTitle="Site Recovery (VMM to VMM)/Site Recovery provider setup and registration"
    description="站点恢复（VMM 到 VMM）/站点恢复提供程序的安装和注册"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="anoopkv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536454"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# 站点恢复（VMM 到 VMM）/站点恢复提供程序的安装和注册
## **建议的步骤**
安装和注册过程中出现的常见问题

* 确保安装 **Microsoft Azure Site Recovery 提供程序**的服务器有权访问以下 URL<br>
    1. *.hypervrecoverymanager.windowsazure.com
    2. *.accesscontrol.windows.net
    3. *.store.core.windows.net

* 确保安装 **Microsoft Azure Site Recovery 提供程序**的服务器上的时钟已根据其目标时区设置了正确的时间。


* 如果你知道要安装 **Microsoft Azure Site Recovery 提供程序**的服务器在代理服务器后面，请始终选择“使用代理服务器连接到 Azure Site Recovery”选项。<br>
    * 随时可以通过运行 **DRConfigurator.exe** 并重新注册 Microsoft Azure Site Recovery 提供程序来更改此设置。


## **建议的文档**
[本地先决条件](https://azure.microsoft.com/documentation/articles/site-recovery-vmm-to-vmm/#on-premises-prerequisites)



<!--HONumber=Aug16_HO3-->



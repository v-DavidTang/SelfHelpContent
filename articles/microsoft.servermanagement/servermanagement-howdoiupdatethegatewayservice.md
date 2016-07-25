<properties
    pageTitle="如何更新网关服务？"
    description="如何更新 Server 管理工具网关服务？"
    service="microsoft.servermanagement"
    resource="gateways"
    authors="jol"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 如何更新网关服务？

## **建议的步骤**

* 可以在“网关更新”边栏选项卡中，将网关更新配置为自动或手动发生。 如果选择“自动”，则会在更新可用后的 30 分钟内安装该项更新。 如果选择“手动”，则需要选择“立即计划”，以计划在接下来的 30 分钟内执行一次性更新。
* 如果需要立即更新，可以重新启动网关服务。 登录到网关计算机，运行“services.msc”启动“服务”MMC 管理单元。 重新启动“ServerManagementToolsGateway”服务，然后在几分钟内将会执行更新。




<!--HONumber=Jul16_HO3-->



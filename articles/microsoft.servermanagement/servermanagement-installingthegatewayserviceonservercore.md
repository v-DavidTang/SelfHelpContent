<properties
    pageTitle="Installing the gateway service on Server Core"
    description="如何在 Windows Server Core 上安装 Server 管理工具网关"
    service="microsoft.servermanagement"
    resource="gateways"
    authors="jol"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 在 Server Core 上安装网关服务

## **建议的步骤**

* 可以在 Windows Server 2012/R2、Windows Server 2016 完全安装版或 Server Core 上安装网关服务。 若要在 Server Core 上安装，请通过命令行使用以下命令安装 GatewayService.msi。 需要使用一个证书来安全地存储用于连接到目标计算机的凭据，而使用以下命令选项可以生成一个自签名证书来实现此目的。<br>
**GatewayService.msi /qn GATEWAYPROFILEJSON=.\profile.json ACCEPTEULA=true ACCEPTPRIVACYPOLICY=true**
* 若要使用计算机上安装的现有证书，请使用以下命令选项。 将 **EnterThumbprintHere** 替换为你的证书加密指纹。<br>
**GatewayService.msi /qn GATEWAYPROFILEJSON=.\profile.json ACCEPTEULA=true ACCEPTPRIVACYPOLICY=true ENCRYPTION_CERTIFICATE_OPTION=root ENCRYPTION_THUMBPRINT=EnterThumbprintHere**




<!--HONumber=Jul16_HO3-->



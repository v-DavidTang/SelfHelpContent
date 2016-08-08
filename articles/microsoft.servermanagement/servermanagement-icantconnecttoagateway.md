<properties
    pageTitle="I can’t connect to a gateway"
    description="无法连接到 Server 管理工具网关"
    service="microsoft.servermanagement"
    resource="gateways"
    authors="jol"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 无法连接到网关

## **建议的步骤**
若要解决常见问题，请尝试下面的一种或多种方法。

* 确保网关边栏选项卡中的“运行状况”状态显示为“正常”，并且未显示任何其他错误或警告。
* 登录到网关计算机，并确保它能够连接到公共 Internet。
* 运行“services.msc”以启动“服务”MMC 管理单元，并确保“ServerManagementToolsGateway”服务正在运行。 此外，请尝试重新启动该服务。
* 确保网关计算机上的系统日期/时间正确。 如果网关与 Azure 服务“Server 管理工具”之间的系统时间相差 15 分钟以上，网关授权将会失败。
* 你可以尝试重新安装网关部署包。 在网关计算机上，转到“程序和功能”并卸载“Server 管理工具网关”。 [生成网关部署包](data-blade:Microsoft_Azure_RSMT.GatewaySetupBlade)，然后下载该包并将它安装在网关计算机上。

## **建议的文档**
[Server 管理工具简介](https://blogs.technet.microsoft.com/nanoserver/2016/02/09/introducing-server-management-tools/)



<!--HONumber=Aug16_HO1-->



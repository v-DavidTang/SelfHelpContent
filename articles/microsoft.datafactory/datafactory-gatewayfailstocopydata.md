<properties 
    pageTitle="Data Management Gateway fails to copy data" 
    description="数据管理网关无法与本地数据存储来回复制数据" 
    service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="4"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>


# 数据管理网关无法与本地数据存储来回复制数据

## **建议的步骤**

- 可以在 Windows 事件日志中的网关日志内找到详细信息。 可以使用 Windows **事件查看器**在“应用程序和服务日志” > “数据管理网关”下面找到这些信息。在排查网关相关的问题时，可以在事件查看器中查找错误级别事件。
- 如果在**更改证书**后网关停止工作，请使用 Microsoft 数据管理网关配置管理器工具或“服务”控制面板小程序，来重新启动（停止再启动）**数据管理网关服务**。 如果仍出现错误，你可能需要向数据管理网关服务用户提供明确的权限，使其能够在证书管理器 (certmgr.msc) 中访问证书。  该服务的默认用户帐户是：**NT Service\DIAHostService**。 
- 当你在数据工厂编辑器中单击“加密”按钮时，如果**凭据管理器**应用程序无法**加密**凭据，请确认你是否在安装了网关的计算机上运行此应用程序。 如果不是，请在网关计算机上运行该应用程序并尝试加密凭据。  
- 如果你看到数据存储连接错误或驱动程序相关的错误，请在网关计算机上启动“数据管理网关配置管理器”，切换到“诊断”选项卡上，为“使用此网关测试与本地数据源的连接”组中的字段选择/输入适当的值，然后单击“测试连接”以确定是否能够使用连接信息和凭据从网关计算机连接到本地数据源。 如果在安装驱动程序后测试连接仍然失败，请重新启动网关以便选择最新的更改。  

## **建议的文档**
[使用数据管理网关在本地与云之间移动数据](https://azure.microsoft.com/documentation/articles/data-factory-move-data-between-onprem-and-cloud/)


<!--HONumber=Jul16_HO1-->



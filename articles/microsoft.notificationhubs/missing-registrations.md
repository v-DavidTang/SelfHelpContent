<properties
    pageTitle="My devices/registrations disappeared from my hub after push."
    description="推送后我的设备/注册信息从中心消失。"
    service="microsoft.notificationhubs"
    authors="locphan"
    displayOrder="6"
    selfHelpType="resource"
    resource="namespaces"
    resourceTags="notificationHubs"
    productPesIds=""
    supportToicIds =""
    cloudEnvironments="public"
/>


# 推送后我的设备/注册信息从中心消失。

## **建议的步骤**
* 检查是否正确配置了[推送通知服务](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices)凭据。<br>
* 检查推送通知服务凭据模式和应用模式是否均为“沙箱”或“生产”。<br>
* 验证在删除令牌已过期的设备后，每当获取最新令牌时，是否能够在通知中心上注册。<br>



<!--HONumber=Aug16_HO4-->



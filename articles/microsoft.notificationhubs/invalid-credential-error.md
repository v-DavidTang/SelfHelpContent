<properties
    pageTitle="I am getting 'Invalid credentials' or 'Failed to validate credentials' errors"
    description="我收到“凭据无效”或“无法验证凭据”错误"
    service="microsoft.notificationhubs"
    authors="locphan"
    displayOrder="3"
    selfHelpType="resource"
    resource="namespaces"
    resourceTags="notificationHubs"
    productPesIds=""
    supportToicIds =""
    cloudEnvironments="public"
/>


# 我收到“凭据无效”或“无法验证凭据”错误

## **建议的步骤**
* 检查是否正确配置了[推送通知服务](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices)凭据。<br>
* (APNS) 检查导出的密钥链证书是否仅包含证书，而不是同时包含密钥和证书。<br>
* 在各种开发人员门户中启用平台通知系统（例如，在 Google Developer 中为 Android 启用 GCM、在 Apple Developer Center 启用推送、将 Windows 应用链接到 Windows 应用商店，等等）。<br>
* 如果适用，请在客户端应用中启用推送。<br>



<!--HONumber=Aug16_HO4-->



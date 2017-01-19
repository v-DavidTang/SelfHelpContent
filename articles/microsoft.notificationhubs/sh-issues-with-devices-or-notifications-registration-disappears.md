<properties
    pageTitle="有关设备或通知的问题/注册信息消失"
    description="有关设备或通知的问题/注册信息消失"
    service="microsoft.notificationhubs"
    authors="faridabharmal"
    displayOrder=""
    selfHelpType="generic"
    resource="namespaces"
    resourceTags="notificationHubs"
    productPesIds="15973"
    supportTopicIds="32565574"
    cloudEnvironments="public"
/>


# <a name="issues-with-devices-or-notificationsregistration-disappears"></a>有关设备或通知的问题/注册信息消失

## <a name="recommended-steps"></a>**建议的步骤**
注册信息消失通常是由于无效 PNS 句柄或无效令牌所致。<br>

* 检查是否正确配置了[推送通知服务](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices)凭据。<br>
* 检查推送通知服务凭据模式和应用模式是否均为“沙箱”或“生产”。<br>
* 验证在删除令牌已过期的设备后，每当获取最新令牌时，是否能够在通知中心上注册。<br>

## <a name="recommended-documents"></a>**建议的文档**
* [诊断指南](http://go.microsoft.com/fwlink/?LinkID=824681)<br>


<!--HONumber=Jan17_HO2-->



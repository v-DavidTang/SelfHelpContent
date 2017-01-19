<properties
    pageTitle="有关设备或通知的问题/未收到推送通知"
    description="有关设备或通知的问题/未收到推送通知"
    service="microsoft.notificationhubs"
    authors="faridabharmal"
    displayOrder=""
    selfHelpType="generic"
    resource="namespaces"
    resourceTags="notificationHubs"
    productPesIds="15973"
    supportTopicIds="32565573"
    cloudEnvironments="public"
/>


# <a name="issues-with-devices-or-notificationspush-notification-not-received"></a>有关设备或通知的问题/未收到推送通知

## <a name="recommended-steps"></a>**建议的步骤**
常见的原因是设备未处于联机状态、设备的网络连接不正常或设备的 PNS 句柄无效。<br>
通知中心仅保证发送，但不保证传送。

* 检查用于注册和发送的通知中心名称以及通知中心设置是否匹配。<br>
* 检查客户端和后端上的 [SAS 配置字符串](data-blade:Microsoft_Azure_NotificationHubs.AccessPolicyGridBlade)是否正确。<br>
* 检查是否正确配置了[平台通知系统](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices)凭据。<br>
* [检查所有设备是否注册](http://go.microsoft.com/fwlink/?LinkID=824679)。<br>
* 检查设备是否已通过 Wifi 或数据网络联机。<br>
* [测试发送](data-blade:Microsoft_Azure_NotificationHubs.TestSendBlade)<br>
* [调试失败的通知](http://go.microsoft.com/fwlink/?LinkID=824680)<br>
* 使用[按消息遥测](http://go.microsoft.com/fwlink/?LinkID=824689)<br>

## <a name="recommended-documents"></a>**建议的文档**
* [诊断指南](http://go.microsoft.com/fwlink/?LinkID=824681)<br>
* [常见错误代码](http://go.microsoft.com/fwlink/?LinkID=824682)<br>
* [遥测指南](http://go.microsoft.com/fwlink/?LinkID=824683)<br>



<!--HONumber=Jan17_HO2-->



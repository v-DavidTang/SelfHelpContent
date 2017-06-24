<properties
    pageTitle="Set up iOS and Mac device management"
    description="设置 iOS 和 Mac 设备管理"
    service="microsoft.intune"
    resource="intune"
    authors="mackie1604"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32530435"
    resourceTags=""
    productPesIds="15584"
    cloudEnvironments="public"
/>


# <a name="intune-enrollment-ios-and-mac"></a>Intune 登记 - iOS 和 Mac

## <a name="recommended-steps"></a>**建议的步骤**

下面是最终用户在 Intune 中登记 iOS 设备时可能会看到的错误列表。

**错误消息：已达到设备上限**

* 在登记另一个移动设备之前，用户必须从公司门户中删除当前已登记的某个移动设备。

**错误消息：无登记策略、APNSCertificateNotValid 或 AccountNotOnboarded**

* Apple Push Notification 服务 (APNs) 提供一个通道用于访问已登记的 iOS 设备。 如果未执行获取 APNs 证书的步骤或者 APNs 证书已过期，则登记尝试将会失败并显示此消息。

**错误消息：DeviceTypeNotSupported**

* 确保用户的设备正在运行 iOS 8.0 或更高版本。

**错误消息：MdmAuthorityNotDefined**

* 未在 Intune 中指定移动设备管理机构。

## <a name="recommended-documents"></a>**建议的文档**

[排查 Intune 中的设备登记问题](https://docs.microsoft.com/intune/troubleshoot/troubleshoot-device-enrollment-in-intune)<br>
[设置 iOS 和 Mac 设备管理](https://docs.microsoft.com/intune/deploy-use/set-up-ios-and-mac-management-with-microsoft-intune)<br>
[登记企业拥有的设备登记计划 - iOS 设备](https://docs.microsoft.com/intune/deploy-use/ios-device-enrollment-program-in-microsoft-intune#steps-to-enroll-ios-devices-by-using-apple-dep-management)<br>
[Microsoft Intune 中的 Wi-Fi 连接](https://docs.microsoft.com/intune/deploy-use/wi-fi-connections-in-microsoft-intune)<br>
[Azure AD 联合身份验证兼容性列表](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-compatibility)<br>
[将 Intune 许可证分配到用户帐户](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune-step-4)<br>
[使用 Office 365 PowerShell 查看已许可和已许可的用户](https://technet.microsoft.com/library/dn771772.aspx)<br>
[在 Intune 中登记 macOS 设备](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-macos)<br>





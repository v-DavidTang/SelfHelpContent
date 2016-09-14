<properties 
    pageTitle="The MAM without enrollment policy is not working for Skype for Business on iOS and Android devices"
    description="不包含注册策略的 MAM 对 iOS 和 Android 设备上的 Skype for Business 不起作用"
    service="microsoft.intune"
    resource="intune"
    authors="JordanWallach"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="mam, mampolicy"
    productPesIds=""
    cloudEnvironments="public"
 />


# 不包含注册策略的 MAM 对 iOS 和 Android 设备上的 Skype for Business 不起作用

## **建议的步骤**
必须使用新式验证设置 Skype for Business。 执行以下步骤：

1. 使用远程 PowerShell 连接到 Skype for Business Online 
2. 运行以下命令：<br>
   `Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed`
3. 运行以下命令，验证更改是否成功：<br>
   `Get-CsOAuthConfiguration` 

## **建议的文档**

[Skype for Business Online：为租户启用新式验证](http://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br>
[使用 Windows PowerShell 连接到 Skype for Business Online](https://aka.ms/SkypePowerShell) <br>
[准备好使用 Microsoft Intune 配置移动应用管理策略](https://docs.microsoft.com/intune/deploy-use/get-ready-to-configure-mobile-app-management-policies-with-microsoft-intune)



<!--HONumber=Sep16_HO1-->



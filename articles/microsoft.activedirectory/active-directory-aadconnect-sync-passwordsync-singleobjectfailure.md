<properties
    pageTitle="Password synchronization does not work for specific user"
    description="特定的用户无法使用密码同步"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="1222"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="password-synchronization-does-not-work-for-specific-user"></a>特定的用户无法使用密码同步

## <a name="recommended-steps"></a>**建议的步骤**
常见的根本原因包括：

* 为本地 Active Directory 用户对象启用了“用户下次登录时必须更改密码”选项。 如果启用此选项，将为该用户分配一个临时密码。该用户下次登录时，系统会提示其更改密码。 Azure AD Connect 不会将临时密码同步到 Azure AD。 若要解决此问题，请执行以下操作之一：
  * 要求该用户登录到本地应用程序（例如 Windows 桌面）并更改密码。 新密码将同步到 Azure AD；或者
  * 让管理员更新该用户的密码且不启用选项“用户下次登录时必须更改密码”选项，并与该用户共享新密码。

* 未针对对象同步或密码同步正确配置本地 Active Directory 用户对象。 若要解决该问题，请遵循[使用 Azure AD Connect 同步排查密码同步问题 - 一个对象不同步密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization#one-object-is-not-synchronizing-passwords)文章部分中所述的步骤。


## <a name="recommended-documents"></a>**建议的文档**
* [使用 Azure AD Connect 同步实现密码同步](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization)  
* [使用 Azure AD Connect 同步排查密码同步问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization)  


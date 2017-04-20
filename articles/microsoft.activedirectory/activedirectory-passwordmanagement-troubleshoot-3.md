<properties
    pageTitle="Tip 4: DEPLOYMENT - Use password reset to obviate the need to communicate temporary passwords"
    description="从客户体验总结的重要提示 - 提示 4"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="400"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public"
 />

# <a name="tip-4-deployment---bypass-temporary-passwords"></a>提示 4：部署 - 绕过临时密码
## <a name="use-password-reset-to-obviate-the-need-to-communicate-temporary-passwords"></a>使用密码重置，避免向用户发送临时密码
这是对提示 3 的补充。 针对密码重置预配置用户以后，设想一下这样一个场景：一位雇员首次加入你的公司。 你现在可以直接让其导航到 [Azure AD 密码重置门户](https://passwordreset.microsoftonline.com)来重置其密码，而不必向其发送临时密码。

使用[已加入 Windows 10 Azure AD 域的设备](https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-devices-group-policy)的用户甚至可以直接从 Windows 10 的现成登录屏幕执行该操作，在你无需为其提供任何帮助的情况下轻松访问全新的电脑。

若要了解如何通过 API、PowerShell 或 Azure AD Connect 执行该操作，请阅读以下文档。 预填充该数据后，只需让用户重置其密码，他们即可访问自己的帐户：
* [在无需用户注册的情况下部署密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#deploying-password-reset-without-requiring-end-user-registration)
* [密码重置使用哪些数据](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#what-data-is-used-by-password-reset)





[在 DOCS.com 上查看](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-4-deployment---use-password-reset-to-obviate-the-need-to-communicate-temporary-passwords)

## <a name="recommended-documents"></a>**建议的文档**
* [在无需用户注册的情况下部署密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#deploying-password-reset-without-requiring-end-user-registration)
* [密码重置使用哪些数据](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#what-data-is-used-by-password-reset)
* [从客户体验总结的重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [常见问题解答 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [故障排除 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)


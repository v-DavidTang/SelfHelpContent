<properties
  pageTitle="Cloud-based MFA/Installing or configuring cloud-based MFA AD FS adapter"
  description="安装或配置基于云的 MFA AD FS 适配器"
  service="microsoft.multifactorauthentication"
  resource=""
  authors="kgremban"
  selfHelpType="generic"
  supportTopicIds="32570991"
  productPesIds="14947"
  cloudEnvironments="public"
/>


# <a name="installing-or-configuring-cloud-based-mfa-ad-fs-adapter"></a>安装或配置基于云的 MFA AD FS 适配器

## <a name="recommended-steps"></a>**建议的步骤**

在 Server 2016 上为基于云的 MFA 配置 AD FS 适配器时，可将 AD FS 适配器用于主要身份验证或辅助身份验证。 用于主要身份验证时，用户必须使用移动应用中的验证作为验证方法。 用于辅助身份验证时，用户可以使用所有已注册的方法（电话呼叫、短信、移动应用通知和移动应用验证码）。

考虑将 AD FS 适配器用于辅助身份验证时，有其他几种备选方法：

1. 对于基于 Web 的应用，由 AAD MFA 执行 MFA 可能更有效。

2. 对于本地应用，可以使用 AAD 应用程序代理，而不要让 AAD 执行 MFA。 

## <a name="recommended-documents"></a>**建议的文档**

[配置 AD FS 2016 和 Azure MFA](https://technet.microsoft.com/windows-server-docs/identity/ad-fs/operations/configure-ad-fs-2016-and-azure-mfa) 
[Active Directory 应用程序代理入门](https://docs.microsoft.com/azure/active-directory/active-directory-application-proxy-get-started) 
[使用 Azure 多重身份验证和 AD FS 保护云资源](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-cloud)

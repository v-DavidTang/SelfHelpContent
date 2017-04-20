<properties
    pageTitle="Microsoft Graph authorization failures"
    description="Microsoft Graph 授权失败"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="PatAltimore"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32134056"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="microsoft-graph-authorization-failures"></a>Microsoft Graph 授权失败

多种不同的问题可能会导致授权失败。 应用的[身份验证流](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-scenarios)、配置的[范围](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-scopes)和[许可](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent)可能会造成授权失败。 本文重点介绍常见的授权失败。

## <a name="understanding-user-and-administrator-consent-for-your-apps"></a>了解用户和管理员对应用的许可

[如何使用多租户应用程序模式将任何 Azure Active Directory (AD) 用户登录](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent)<br>
[Azure Active Directory v2.0 终结点中的范围、权限和许可](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-scopes)<br>
[在 Azure AD 与 Azure AD v2.0 终结点之间做出决定](https://developer.microsoft.com/graph/docs/authorization/auth_overview#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints)

## <a name="how-do-my-apps-get-access-to-customer-data-using-consent-what-is-a-multi-tenant-app"></a>应用如何使用许可获取客户数据的访问权限？ 什么是多租户应用？

[如何使用多租户应用程序模式将任何 Azure Active Directory (AD) 用户登录](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent)

## <a name="choosing-required-permissions-for-your-app"></a>为应用选择所需的权限

[Microsoft Graph 权限范围](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Azure AD Graph 权限范围](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)

## <a name="i-get-a-403-forbidden-but-i-selected-all-permissions"></a>我选择了所有权限，但还是收到“403 禁止访问”错误

对于委派的交互式代码流，Microsoft Graph 将会根据授予应用的权限以及用户拥有的权限来评估是否允许请求。  “403 禁止访问”错误指示用户没有足够的特权，无法执行请求。  只有拥有所需权限的用户才能成功发出请求。

[Microsoft Graph 权限范围](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Azure AD Graph 权限范围](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)

## <a name="what-do-i-do-when-i-get-a-401-unauthorized-error-even-though-i-selected-all-the-permissions"></a>如果即使选择了所有权限也出现“401 未授权”错误，该怎么办？

* 如果授予了应用程序权限但使用委派的交互式代码流来获取令牌，可能会收到“未授权”错误。 向应用授予应用程序权限时，请使用客户端凭据后台程序服务到服务流来获取令牌。<br>
[Azure Active Directory v2.0 和 OAuth 2.0 客户端凭据流](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)<br>
* 如果授予了委派权限但使用客户端凭据后台程序服务到服务流来获取令牌，可能会收到“未授权”错误。 向应用授予委派权限时，请使用委派的交互式代码流来获取令牌。<br>
[使用 OAuth 2.0 授权代码授予通过 AAD Graph 对目录进行委派访问](https://blogs.msdn.microsoft.com/aadgraphteam/2013/05/16/using-oauth-2-0-authorization-code-grant-for-delegated-access-of-directory-via-aad-graph/)

[Microsoft Graph 权限范围](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Azure AD Graph 权限范围](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)

## <a name="i-configured-the-app-in-my-tenant-with-the-permissions-it-needs-but-i-still-get-a-401-unauthorized-error-when-trying-to-use-it"></a>我在租户中使用所需的权限配置了应用，但尝试使用该应用时仍收到“401 未授权”错误

1. 在 Azure 门户中 Web 客户端应用程序的配置页上，使用“所需权限”部分中的菜单设置应用程序所需的权限。<br>
2. 当应用在 Azure AD 中进行身份验证时，如果尚未授予许可，Azure AD 将提示用户授予许可，并显示运行该应用程序所需的权限。
3. 管理员可以代表租户中的所有用户许可应用程序的委派权限。 管理员可通过 Azure 门户执行此操作。 在应用程序的“设置”边栏选项卡中单击“所需权限”，然后单击“授予权限”按钮。

[许可框架的概述](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#overview-of-the-consent-framework)<br>
[将应用程序与 Azure Active Directory 集成](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications)

## <a name="i-tried-to-delete-users-or-reset-passwords-but-i-get-a-401-unauthorized"></a>我已尝试删除用户或重置密码，但收到“401 未授权”错误

应用程序使用的后台程序服务到服务权限目前不支持这些高特权操作。  请以登录管理员的身份使用交互式代码流。

[Microsoft Graph 权限范围](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Azure AD Graph 权限范围](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)


<properties
    pageTitle="Microsoft Graph authentication token issues"
    description="Microsoft Graph 身份验证令牌问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="PatAltimore"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32134055"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="microsoft-graph-authentication-token-issues"></a>Microsoft Graph 身份验证令牌问题

## <a name="how-do-i-authenticate-and-authorize-graph-apis"></a>如何对图形 API 进行身份验证和授权？

若要为应用授权，首先请对用户进行身份验证。 为此，可将用户重定向到 Azure Active Directory (Azure AD) 授权终结点并提供应用信息，让他们登录到其工作或学校帐户。 用户登录并许可应用请求的权限（如果用户尚未这样做）后，应用将会收到用于获取 OAuth 访问令牌的授权代码。

[使用 Azure AD 进行 Microsoft Graph 应用身份验证](https://developer.microsoft.com/graph/docs/authorization/app_authorization)

## <a name="how-do-i-call-microsoft-graph-from-a-daemon-service-where-there-is-no-user-signed-in"></a>如何从用户没有登录过的后台程序服务调用 Microsoft Graph？

对于服务或后台程序应用，应用程序应实现 OAuth 2.0 客户端凭据授予流。 调用 Microsoft Graph 时，应用将使用自身的凭据、客户端 ID 和应用程序密钥进行身份验证，而不是模拟用户。

[在服务或后台程序应用中调用 Microsoft Graph](https://developer.microsoft.com/graph/docs/authorization/app_only)


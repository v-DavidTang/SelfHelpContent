 <properties
    pageTitle="Business to Consumer (B2C)/Password reset failing"
    description="企业对消费者 (B2C)/密码重置失败"
    service="microsoft.azureactivedirectory"
    resource="b2cDirectories"
    authors="parakhj"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds="32416703"
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="password-reset-link-is-not-working"></a>密码重置链接不起作用

目前，组合的“注册或登录策略”有一个限制，该限制可防止用户能够从登录页重置其密码。 用户单击密码重置链接时，Azure AD B2C 将向应用程序返回错误。 在这种情况下，有两种实现密码重置的不同机制：

1. **使用登录策略**：应用程序不需要工作，单击“我忘记了密码”会将用户自动重定向到通用的带 Microsoft 商标的密码重置页。
1. **处理错误**：这将需要应用程序执行一些额外的工作。 单击“我忘记了密码”会将用户重定向回应用程序并提供一个错误代码。 应用程序需要检测请求中的错误代码，然后进一步将用户重定向到 Azure AD B2C 密码重置策略。 密码重置策略可以广泛地自定义。

## <a name="recommended-documents"></a>**建议的文档**

[使用注册或登录策略的示例](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-web-dotnet-susi)

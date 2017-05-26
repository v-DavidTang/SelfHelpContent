 <properties
    pageTitle="Business to Consumer (B2C)"
    description="企业对消费者 (B2C)"
    service="microsoft.azureactivedirectory"
    resource="b2cDirectories"
    authors="parakhj"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32422332"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="business-to-consumer-b2c"></a>企业对消费者 (B2C)

## <a name="recommended-steps"></a>**建议的步骤**

### <a name="password-reset-link-is-not-working"></a>**密码重置链接不起作用**

目前，组合的“注册或登录策略”有一个限制，该限制可防止用户能够从登录页重置其密码。 用户单击密码重置链接时，Azure AD B2C 将向应用程序返回错误。 在这种情况下，有两种实现密码重置的不同机制：

1. **使用登录策略**：应用程序不需要工作，单击“我忘记了密码”会将用户自动重定向到通用的带 Microsoft 商标的密码重置页。
1. **处理错误**：这将需要应用程序执行一些额外的工作。 单击“我忘记了密码”会将用户重定向回应用程序并提供一个错误代码。 应用程序需要检测请求中的错误代码，然后进一步将用户重定向到 Azure AD B2C 密码重置策略。 密码重置策略可以广泛地自定义。

### <a name="session-token-configuration-is-not-being-enforced"></a>**未强制实施会话令牌配置**

如果使用“登录”策略，则不会强制使用你的自定义会话令牌持续时间。 解决方法是改用组合的“登录/注册”策略。 此问题源于以下事实：“注册或登录”策略利用了与旧版“登录”策略相比而言更新或已改进的策略实施。

### <a name="i-am-unable-to-customize-the-ui"></a>**无法自定义 UI**

目前，对于“登录”策略，我们不支持 UI 自定义。 如果要自定义登录页，可以使用“注册或登录”策略。 如果要查看“登录”策略支持的 UI 自定义，我们鼓励你在 [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/suggestions/13062033-b2c-fully-customizable-sign-in-page) 论坛中投票并/或添加评论，同时提供反馈。

## <a name="recommended-documents"></a>**建议的文档**

* [Azure AD B2C 策略](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies)
* [常见问题](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs)
* [堆栈溢出](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
* [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)

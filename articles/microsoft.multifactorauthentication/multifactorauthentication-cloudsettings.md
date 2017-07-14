<properties  
    pageTitle="Cloud-based MFA/Configuring Azure MFA Settings"
    description="排查 Azure MFA 设置问题"
    service="microsoft.multifactorauthentication"
    resource=""
    authors="kgremban"
    selfHelpType="generic"
    supportTopicIds="32570990"
    productPesIds="14947"
    cloudEnvironments="public"
    />


# 配置 Azure MFA 设置
<a id="configuring-azure-mfa-settings" class="xliff"></a>

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>

1. **强制许可** – 你需要负责确保为 Azure MFA 提供适当的许可证。 Azure MFA 门户不会验证是否为选择使用 Azure MFA 保护的所有用户和管理员提供了足够的许可证。

2. **注册** – 若要使用 Azure MFA，用户必须先注册一种验证方法。 如果你通过将用户的 MFA 状态设置为“已启用”来启用基于用户的 MFA，则用户下次登录时，系统会提示其注册安全信息。 如果使用条件访问来要求执行 MFA，则应将用户的 MFA 状态保留为“已禁用”并将用户指向 MFA 注册门户（https://aka.ms/mfasetup ->“其他安全验证”），或使用 MFA 注册策略为用户注册 MFA。

3. **自动 MFA 注册** – 尽管可以使用 PowerShell 来设置用户的 MFA 状态，但目前无法以编程方式为 MFA 预先注册用户的电话号码。

## **建议的文档**
<a id="recommended-documents" class="xliff"></a> 

- [云中的 Azure 多重身份验证入门](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-cloud)
- [多重身份验证注册策略](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection#multi-factor-authentication-registration-policy)
- [如何获取 Azure 多重身份验证](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans#how-to-get-azure-multi-factor-authentication-1) 

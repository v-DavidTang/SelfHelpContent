<properties  
    pageTitle="Cloud-based MFA/Installing or configuring Azure MFA NPS extension" 
    description="安装或配置 MFA 服务（云）的扩展" 
    service="microsoft.multifactorauthentication" 
    resource="" 
    authors="kgremban" 
    selfHelpType="generic" 
    supportTopicIds="32565586" 
    productPesIds="14947" 
    cloudEnvironments="public"
    />
 

# <a name="installing-or-configuring-extensions-for-mfa-service-cloud"></a>安装或配置 MFA 服务（云）的扩展  
## <a name="recommended-steps"></a>**建议的步骤** 
请遵循以下步骤，使用 Azure MFA 的 NPS 扩展排查常见方案的问题： 

**ADAL 令牌错误**
<!---Loc Comment: The matada seems to be incorrect--->
1. 重新启动 NPS 服务器。 
2. 验证是否已按预期安装了客户端证书。 
3. 验证该证书是否与 AzureAD 上的租户关联。 
4. 验证是否可以从运行该扩展的服务器访问 https://login.windows.net/。 

**HTTP 日志显示“找不到用户”错误**

1. 验证 AD Connect 是否正在运行。 
2. 验证该用户是否在 Windows Active Directory 和 Azure Active Directory 中存在。 可根据 UPN 或备用登录 ID 来判断某个用户是否存在。 这些信息应在本地 AD 与 Azure AD 之间同步。 

**NoDefaultAuthenticationMethodIsConfigured 和 ProofDataNotFound**

1. 验证该用户是否已注册 Azure MFA 并至少设置了一种验证方法。 

**日志中包含 HTTP 连接错误，并且所有身份验证失败**

1. 验证是否可以从运行 NPS 扩展的服务器访问 https://adnotifications.windowsazure.com。 

## <a name="recommended-documents"></a>**建议的文档** 
  
- [将现有 NPS 基础结构与 Azure 多重身份验证集成](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-nps-extension) 
- [解决 Azure 多重身份验证的 NPS 扩展出现的错误消息](https://review.docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-nps-errors?branch=pr-en-us-10717)


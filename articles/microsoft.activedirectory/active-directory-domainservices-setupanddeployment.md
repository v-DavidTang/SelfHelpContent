<properties
    pageTitle="Setup and deployment of Azure AD Domain Services"
    description="Azure AD 域服务"
    service="microsoft.aad"
    resource="Microsoft_AAD_DomainServices"
    authors="arluca"
    selfHelpType="generic"
    supportTopicIds="32447391"
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="setup-and-deployment-of-azure-ad-domain-services"></a>Azure AD 域服务的设置和部署

## <a name="unable-to-enable-azure-ad-domain-services-for-your-azure-ad-directory"></a>无法为 Azure AD 目录启用 Azure AD 域服务。 

单击出现的错误消息显示相应的故障排除步骤：

*    [名称 contoso100.com 已在此网络中使用。指定一个未使用的名称。](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#domain-name-conflict)
*    [无法在此 Azure AD 租户中启用域服务。该服务对名为“Azure AD 域服务同步”的应用程序没有足够的权限。请删除名为“Azure AD 域服务同步”的应用程序，然后尝试为 Azure AD 租户启用域服务。](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#inadequate-permissions)
*    [无法在此 Azure AD 租户中启用域服务。Azure AD 租户中的域服务应用程序没有所需的权限来启用域服务。请删除标识符为 d87dcbc6-a371-462e-88e3-28ad15ec4e64 的应用程序，然后尝试为 Azure AD 租户启用域服务。](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#invalid-configuration)
*    [无法在此 Azure AD 租户中启用域服务。Microsoft Azure AD 应用程序已在你的 Azure AD 租户中禁用。请启用标识符为 00000002-0000-0000-c000-000000000000 的应用程序，然后尝试为 Azure AD 租户启用域服务。](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#microsoft-graph-disabled.)

## <a name="users-are-unable-to-sign-in-to-the-azure-ad-domain-services-managed-domain"></a>用户无法登录 Azure AD 域服务托管域

1.    尝试使用 UPN 格式（例如“joeuser@contoso.com”）而不是 SAMAccountName 格式（例如“CONTOSO\joeuser”）登录。 
2.    确保根据《入门指南》中所述的步骤[启用密码同步](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync)。
3.    注意：确保受影响的用户帐户不是 Azure AD 租户中的外部帐户。 由于 Azure AD 域服务没有此类用户帐户的凭据，因此外部用户无法登录到托管域。
4.    如果受影响的用户帐户是仅限云的用户帐户：确保在你启用 Azure AD 域服务之后，用户已更改其密码。 执行此步骤可以生成 Azure AD 域服务所需的凭据哈希。
5.    如果受影响的用户帐户已从本地目录同步：确认[建议的 Azure AD Connect 版本](https://www.microsoft.com/download/details.aspx?id=47594)已配置为[执行完全同步](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync)。
6.    如果确认步骤 4 之后仍然出现问题，请在同步计算机上执行以下命令：1. "net stop 'Microsoft Azure AD Sync'" 2. "net start 'Microsoft Azure AD Sync'"

## <a name="recommended-documents"></a>**建议的文档**
* [从 Azure AD 租户中删除的用户不会从托管域中删除](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#users-removed-from-your-azure-ad-tenant-are-not-removed-from-your-managed-domain)
* [你在托管域上不拥有的管理特权](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)
* [Azure AD 域服务常见问题解答](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)


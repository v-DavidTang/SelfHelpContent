<properties
    pageTitle="Enabling and Disabling Azure AD Domain Services"
    description="Azure AD 域服务"
    service="microsoft.aad"
    resource="Microsoft_AAD_DomainServices"
    authors="arluca"
    selfHelpType="generic"
    supportTopicIds="32447391"
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="enabling-and-disabling-azure-ad-domain-services"></a>启用和禁用 Azure AD 域服务

## <a name="unable-to-enable-azure-ad-domain-services-for-your-azure-ad-directory"></a>无法为 Azure AD 目录启用 Azure AD 域服务。 

单击出现的错误消息显示相应的故障排除步骤：

*    [名称 contoso100.com 已在此网络中使用。指定一个未使用的名称。](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#domain-name-conflict)
*    [无法在此 Azure AD 租户中启用域服务。该服务对名为“Azure AD 域服务同步”的应用程序没有足够的权限。请删除名为“Azure AD 域服务同步”的应用程序，然后尝试为 Azure AD 租户启用域服务。](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#inadequate-permissions)
*    [无法在此 Azure AD 租户中启用域服务。Azure AD 租户中的域服务应用程序没有所需的权限来启用域服务。请删除标识符为 d87dcbc6-a371-462e-88e3-28ad15ec4e64 的应用程序，然后尝试为 Azure AD 租户启用域服务。](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#invalid-configuration)
*    [无法在此 Azure AD 租户中启用域服务。Microsoft Azure AD 应用程序已在你的 Azure AD 租户中禁用。请启用标识符为 00000002-0000-0000-c000-000000000000 的应用程序，然后尝试为 Azure AD 租户启用域服务。](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#microsoft-graph-disabled.)

## <a name="recommended-documents"></a>**建议的文档**
* [你在托管域上不拥有的管理特权](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)
* [Azure AD 域服务常见问题解答](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)


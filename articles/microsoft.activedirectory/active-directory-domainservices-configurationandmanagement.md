<properties
    pageTitle="Configuration, Management and Integration issues"
    description="Azure AD 域服务"
    service="microsoft.aad"
    resource="Microsoft_AAD_DomainServices"
    authors="arluca"
    selfHelpType="generic"
    supportTopicIds="32447390"
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="configuration-management-and-integration-issues"></a>配置、管理和集成问题

## <a name="unable-to-complete-certain-administrative-tasks"></a>无法完成某些管理任务

“AAD DC 管理员”组的成员只被授予在托管域上执行以下任务所需的特权：

1.  将计算机加入托管域。
2.  配置托管域中”AADDC 计算机”和”AADDC 用户”容器的内置 GPO。
3.  管理托管域上的 DNS。
4.  在托管域上创建和管理客户组织单位 (OU)。
5.  获取对已加入托管域的计算机的管理访问权限。 

有关详细信息，请参阅[你在托管域上不拥有的管理特权](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)。

## <a name="administrator-unable-to-sign-in-to-the-azure-ad-domain-services-managed-domain"></a>管理员无法登录 Azure AD 域服务托管域

1.  尝试使用 UPN 格式（例如“joeuser@contoso.com”）而不是 SAMAccountName 格式（例如“CONTOSO\joeuser”）登录。
2.  确保根据《入门指南》中所述的步骤[启用密码同步](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync)。
3.  确保所用的虚拟机已加入托管域。 
4.  确保所用的用户帐户属于“AAD DC 管理员”组。

## <a name="recommended-documents"></a>**建议的文档**
* [从 Azure AD 租户中删除的用户不会从托管域中删除](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#users-removed-from-your-azure-ad-tenant-are-not-removed-from-your-managed-domain)
* [你在托管域上不拥有的管理特权](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)
* [Azure AD 域服务 - 故障排除指南](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting)
* [Azure AD 域服务常见问题解答](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)


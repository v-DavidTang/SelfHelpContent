<properties
    pageTitle="Users are unable to sign in to the Azure AD Domain Services managed domain "
    description="Azure AD 域服务"
    service="microsoft.aad"
    resource="Microsoft_AAD_DomainServices"
    authors="arluca"
    selfHelpType="resource"
    displayOrder="200"
    cloudEnvironments="public"
/>


# <a name="users-are-unable-to-sign-in-to-the-azure-ad-domain-services-managed-domain"></a>用户无法登录 Azure AD 域服务托管域

## <a name="recommended-steps"></a>**建议的步骤**
1.    尝试使用 UPN 格式（例如“joeuser@contoso.com”）而不是 SAMAccountName 格式（例如“CONTOSO\joeuser”）登录。 
2.    确保根据《入门指南》中所述的步骤[启用密码同步](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync)。
3.    注意：确保受影响的用户帐户不是 Azure AD 租户中的外部帐户。 由于 Azure AD 域服务没有此类用户帐户的凭据，因此外部用户无法登录到托管域。
4.    如果受影响的用户帐户是仅限云的用户帐户：确保在你启用 Azure AD 域服务之后，用户已更改其密码。 执行此步骤可以生成 Azure AD 域服务所需的凭据哈希。
5.    如果受影响的用户帐户已从本地目录同步：确认[建议的 Azure AD Connect 版本](https://www.microsoft.com/download/details.aspx?id=47594)已配置为[执行完全同步](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync)。
6.    如果确认步骤 4 之后仍然出现问题，请在同步计算机上执行以下命令：1. "net stop 'Microsoft Azure AD Sync'" 2. "net start 'Microsoft Azure AD Sync'"

## <a name="recommended-documents"></a>**建议的文档**
* [你在托管域上不拥有的管理特权](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)
* [Azure AD 域服务常见问题解答](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)


<properties
    pageTitle="Problem removing deleted Azure AD users from your managed domain"
    description="Azure AD 域服务"
    service="microsoft.aad"
    resource="Microsoft_AAD_DomainServices"
    authors="arluca"
    selfHelpType="resource"
    displayOrder="300"
    cloudEnvironments="public"
/>


# <a name="problem-removing-deleted-azure-ad-users-from-your-managed-domain"></a>从托管域中移除已删除的 Azure AD 用户时遇到问题
Azure AD 会防止意外删除用户对象。 如果从 Azure AD 租户中删除某个用户帐户，相应的用户对象将移到回收站。 将此删除操作同步到托管域时，会导致相应的用户帐户标记为已禁用，即使在 Azure AD 目录中使用相同的 UPN 重新创建一个用户帐户，也是如此。 

## <a name="recommended-steps"></a>**建议的步骤**
若要从托管域中删除用户，必须先从 Azure AD 租户中永久删除该用户： 
*  如此 [MSDN 文章](https://msdn.microsoft.com/library/azure/dn194132.aspx)中所述，结合 '-RemoveFromRecycleBin' 选项使用 Remove-MsolUser PowerShell cmdlet 即可。

## <a name="recommended-documents"></a>**建议的文档**
* [Azure AD 域服务常见问题解答](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)


<properties
    pageTitle="I can't delete my domain name"
    description="Azure Active Directory 域疑难解答"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
    displayOrder="4292"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-delete-my-domain-name"></a>无法删除域名

## <a name="recommended-steps"></a>**建议的步骤**

1. 请确保已删除使用了所要删除的域名的所有用户、组和应用程序。 该域名不能有任何依赖项，否则删除将会失败。 [了解详细信息](https://support.microsoft.com/help/2787210/-unable-to-remove-this-domain-error-when-you-try-to-remove-a-domain-from-office-365)。

2. 如果租户中有多个子域，则需要先删除每个子域，然后才能删除根域。 例如，如果使用了 **na.contoso.com** 和**emea.contoso.com**，则必须先删除这些子域，然后才能删除父域 **contoso.com** [了解详细信息](https://support.microsoft.com/help/2787792/-domain-has-associated-subdomains-or-you-cannot-remove-a-domain-that-has-subdomains-error-when-you-try-to-remove-a-domain-from-office-365)。

## <a name="recommended-documents"></a>**建议的文档**

[在 Azure AD 中添加自定义域名](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain)

[用于删除域的 PowerShell](https://docs.microsoft.com/powershell/msonline/v1/remove-msoldomain)


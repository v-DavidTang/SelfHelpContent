<properties
    pageTitle="I can't verify my domain name even though I added it to Azure AD"
    description="Azure Active Directory 域疑难解答"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder="4291"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-verify-my-domain-name-even-though-i-added-it-to-azure-ad"></a>即使已将域名添加到 Azure AD，也无法验证该域名

## <a name="recommended-steps"></a>**建议的步骤**

1. 确保在域名注册机构中正确配置 TXT/MX 记录。  最长可能需要在 72 小时后，该域名才显示为“已验证”。 [了解详细信息](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#add-the-dns-entry-at-the-domain-name-registrar-for-the-domain)

2. 如果以前在另一个 Azure AD 租户或 Office 365 租户中配置了域名，必须通过现有租户排查域的问题。 不能在两个不同的租户中验证同一个自定义域名。 根据设计，这种验证将会失败。 [了解详细信息](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#troubleshooting)

3. 如果你的某些用户已通过自助注册激活 PowerBI 并且你为组织创建了非托管租户，则 IT 管理员可以通过权限接管来管理此租户，或者可以在 PowerShell 中使用强制接管选项继续添加域。 详细了解[管理员域接管](https://powerbi.microsoft.com/documentation/powerbi-admin-administering-power-bi-in-your-organization/#what-is-the-process-to-manage-a-tenant-created-by-Microsoft-for-my-users)。

## <a name="recommended-documents"></a>**建议的文档**

[在 Azure AD 中添加自定义域名](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain)

[联合域名和托管域名](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#federated-and-managed-domain-names)



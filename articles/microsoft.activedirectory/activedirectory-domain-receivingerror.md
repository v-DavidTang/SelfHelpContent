<properties
    pageTitle="Receiving error about domain configured on another tenant"
    description="Azure Active Directory 目录故障排除"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="4299"
    selfHelpType="generic"
    supportTopicIds="32570974"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />


# <a name="receiving-error-about-domain-configured-on-another-tenant"></a>收到了有关域已在其他租户中配置的错误  

## <a name="recommended-steps"></a>**建议的步骤**

1.    不能在两个不同的租户中验证同一个自定义域名。 如果已在 Office 365 中配置自定义域名并尝试将该域名添加到其他 Azure AD 租户，则验证将会失败。 必须先从已验证该域名的现有租户中删除它，然后将它添加到新的 Azure AD 租户。
2.    如果组织中的某人已使用 PowerBI 或 RMS 的自助注册，他们可能已创建非托管租户。 可以使用管理员接管功能来管理此租户，或者在 PowerShell 中使用强制接管选项添加该域。

## <a name="recommended-documents"></a>**建议的文档**

* [将 Azure 订阅所有权转让给其他帐户](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
* [如何执行 DNS 域名接管](https://docs.microsoft.com/azure/active-directory/active-directory-self-service-signup#how-to-perform-a-dns-domain-name-takeover)
* [Office 365 和 Azure AD 租户中的资源依赖关系](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-directory-independence) 


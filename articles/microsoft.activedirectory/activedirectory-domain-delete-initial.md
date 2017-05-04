<properties    
    pageTitle="I want to delete the initial .onmicrosoft.com domain"
    description="Azure Active Directory 域疑难解答"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="4293"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain,domain_directory"
    productPesIds=""
    cloudEnvironments="public"
    />


# <a name="i-want-to-delete-the-initial-onmicrosoftcom-domain"></a>我想要删除初始的 .onmicrosoft.com 域

## <a name="recommended-steps"></a>**建议的步骤**

1. 若要删除现有的 .onmicrosoft.com 域，必须先删除已创建的租户实例， 在删除租户之前，必须先删除所有用户、组和应用程序，并取消 Azure 和/或 Office 365 订阅。 [了解详细信息](https://support.microsoft.com/help/2787210/-unable-to-remove-this-domain-error-when-you-try-to-remove-a-domain-from-office-365)。

2. 如果使用初始 .onmicrosoft.com 域（例如 **myname.onmicrosoft.com**）错误地创建了一个 Azure AD 租户，然后想要将它更新为更友好的公司名称（例如 **contoso.onmicrosoft.com**），可以配置新的 Azure AD 租户并将订阅与目标租户相关联。 [了解详细信息](https://support.microsoft.com/help/2787792/-domain-has-associated-subdomains-or-you-cannot-remove-a-domain-that-has-subdomains-error-when-you-try-to-remove-a-domain-from-office-365)。

## <a name="recommended-documents"></a>**建议的文档**

* [初始域名和自定义域名](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#initial-and-custom-domain-names)
* [Azure AD 和其他 Microsoft Online Services 中的域名](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#domain-names-in-azure-ad-and-other-microsoft-online-services)



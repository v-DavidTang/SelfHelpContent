<properties
    pageTitle="I still have other problems related to domain name management"
    description="Azure Active Directory 域疑难解答"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="4297"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain,domain_directory"
    productPesIds=""
    cloudEnvironments="public"
    />


# <a name="i-still-have-other-problems-related-to-domain-name-management"></a>仍然遇到与域名管理相关的其他问题
 
## <a name="recommended-steps"></a>**建议的步骤** 

若要删除 Azure AD 租户，必须先删除目录中自定义域名的所有关联项，以及目录中的所有用户、组、应用程序与 Azure 和/或 Office 365 订阅。 删除 Azure AD 租户的操作不可逆。 驻留在该目录中的所有数据将永久被删除。 详细了解如何[删除目录](https://docs.microsoft.com/azure/active-directory/active-directory-administer)。

1. 确保你是该目录的全局管理员，并且你是该目录中的唯一用户。 只有在删除所有其他用户后，才能删除该目录。 如果用户是从本地同步的，则需要关闭同步，并且必须使用 Azure 门户或 PowerShell 从云目录中删除这些用户。 
2. 该目录中不能有任何应用程序。 只有在删除所有应用程序后，才能删除该目录。
3. 与该目录相关联的任何 Microsoft Online Services（例如 Microsoft Azure、Office 365 或 Azure AD Premium）不存在任何订阅。 有关 Azure 订阅的详细信息，请参阅[取消 Azure 订阅](https://docs.microsoft.com/azure/active-directory/billing-how-to-cancel-azure-subscription)。
4. 如果你是使用工作或学校帐户登录的，请务必不要尝试删除你的主目录。 例如，如果你已使用 joe@contoso.onmicrosoft.com 登录，则不能删除默认域为 contoso.onmicrosoft.com 的目录。  
5. 不能有任何多重身份验证提供程序链接到该目录。  

## <a name="recommended-documents"></a>**建议的文档** 
 
* [将 Azure 订阅所有权转让给其他帐户](https://docs.microsoft.com/azure/billing/billing-subscription-transfer) 
* [添加自定义域名的子域](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#add-subdomains-of-a-custom-domain)  
* [Office 365 和 Azure AD 租户中的资源依赖关系](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-directory-independence)  
* [使用 PowerShell 或图形 API 管理域名](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#use-powershell-or-graph-api-to-manage-domain-names)  
 
 

<properties
    pageTitle="Problem deleting a domain name"
    description="Azure Active Directory 自助案例提交"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045808"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="problem-deleting-a-domain-name"></a>删除域名时出现问题 

## <a name="recommended-steps"></a>**建议的步骤**
1.    若要删除某个自定义域名，请确保已删除依赖于该自定义域名的所有用户、组和应用程序。 如果有任何现有的资源使用该域名，则删除操作不会成功。 
2.    尝试删除租户“contoso.com”时，请确保用于登录的帐户不是 admin@contoso.com，因为使用该帐户删除不会成功。 必须使用与所要删除的自定义域名之间不存在依赖关系的“全局管理员”帐户，改用类似于 admin@contoso.onmicrosoft.com 的初始默认域名并登录，这样才能删除该域名。 或者，可以使用包含其他已验证域名（例如 admin@contosocorp.com）的“全局管理员”帐户来删除目录中的“contoso.com”。 
3.    如果尝试删除初始默认 Azure AD 域名（例如“contoso.onmicrosoft.com”），该操作不会成功，因为这个三级域是创建目录时建立的。 此初始域名主要用于在验证自定义域名之前进行引导。
4.    如果想要在另一个 Azure AD 租户中或 Office 365 中使用现有的 .onmicrosoft.com 域（例如“contoso.onmicrosoft.com”），必须删除现有的目录，然后使用相同的初始默认名称“contoso.onmicrosoft.com”创建新实例。 数据不会传输到新租户，域名删除操作不可逆。 


## <a name="recommended-documents"></a>**建议的文档**

* [管理 .onmicrosoft.com 初始默认域名](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#initial-and-custom-domain-names) 
* [从 Azure AD 中删除用户]( https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal) 
* [删除目录中的应用程序](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications)
* [域的资源依赖关系](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-directory-independence) 
* [使用 PowerShell 或图形 API 管理域名](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#use-powershell-or-graph-api-to-manage-domain-names) 





<properties 
    pageTitle="I can't create a new user in my Azure AD"
    description="我无法在 Azure AD 中创建新用户"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder="2500"
    selfHelpType="resource"
    resourceTags="userandgroups_overview,userandgroups_user"
    cloudEnvironments="public"
 />

# <a name="i-cant-create-a-new-user-in-my-azure-ad"></a>我无法在 Azure AD 中创建新用户

## <a name="recommended-steps"></a>**建议的步骤**
1. 确保你有权创建新的标准用户。 只有 Azure AD 的全局管理员或用户管理员可以创建新的标准用户。 如果你未充当其中的角色之一，必须让管理员为你创建新用户或者将你添加到这些角色之一。  [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2. 请确保用户名位于本地 AD 中未联合到 Azure AD 的域内。 不能在其域名与 Azure AD 联合的云中添加用户。
3. 请确保没有其他用户或联系人已使用你要分配给新用户的用户名。 用户名必须在整个 Azure AD 中保持唯一。

## <a name="recommended-documents"></a>**建议的文档**

* [使用 Azure 门户在 Azure AD 中创建新用户](https://docs.microsoft.com/azure/active-directory/active-directory-users-create-azure-portal) 
* [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) 
* [使用 Azure AD PowerShell 创建新用户](https://docs.microsoft.com/powershell/azuread/v2/new-azureaduser)



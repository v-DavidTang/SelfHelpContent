<properties
    pageTitle="I can’t delete a user from my directory"
    description=" 无法从目录中删除用户"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder="2570"
    selfHelpType="resource"
    resourceTags="userandgroups_overview,userandgroups_user"
    cloudEnvironments="public"
 />

# <a name="i-cant-delete-a-user-from-my-directory"></a>无法从目录中删除用户

## <a name="recommended-steps"></a>**建议的步骤**

1. 确保你有权删除用户。 只有 Azure AD 的全局管理员或用户管理员可以删除用户。 如果你未充当其中的角色之一，需要让管理员将你添加到这些角色之一，或者为你删除用户。  [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2. 确保未从本地 AD 同步该用户。 如果该用户已同步（即，如果源 =“Windows Server AD”），请在本地目录中删除该用户。 运行同步后，可以看到该用户已从 Azure AD 中删除。

## <a name="recommended-documents"></a>**建议的文档**

* [在 Azure 门户中删除用户](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal)
* [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
* [使用 Azure AD PowerShell 删除用户](https://docs.microsoft.com/powershell/azuread/v2/remove-azureaduser)


 <properties 
    pageTitle="Creating a user or group"
    description="在 Azure AD 中创建、更新或删除用户时出现问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder="2500"
    selfHelpType="generic"
    supportTopicIds="32045780"
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="creating-a-user-or-group"></a>创建用户或组

## <a name="recommended-steps"></a>**建议的步骤**

1. 请确保你有权执行此操作。 只有 Azure AD 中的全局管理员或用户管理员可以创建用户。 如果你未充当其中的角色之一，必须让管理员为你创建新用户或者将你添加到这些角色之一。 [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2. 若要创建新用户，请确保用户名唯一，并且该用户位于本地 AD 中未联合到 Azure AD 的域内。 用户名必须在整个 Azure AD 中保持唯一。 不能在其域名与 Azure AD 联合的云中添加用户。

## <a name="recommended-documents"></a>**建议的文档**

* [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)

* [使用 Azure 门户在 Azure AD 中创建新用户](https://docs.microsoft.com/azure/active-directory/active-directory-users-create-azure-portal) 
* [使用 Azure AD PowerShell 管理组](https://docs.microsoft.com/powershell/module/Azuread/?view=azureadps-2.0#groups)

* [使用 Azure AD PowerShell 管理用户](https://docs.microsoft.com/powershell/azuread/v2/azureactivedirectory#users)


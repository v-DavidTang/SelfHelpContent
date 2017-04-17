 <properties 
    pageTitle="Problem creating, updating, or deleting a user in Azure AD"
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


# <a name="i-cant-create-a-new-user-in-my-azure-ad"></a>我无法在 Azure AD 中创建新用户

## <a name="recommended-steps"></a>**建议的步骤**

1. 请确保你有权执行此操作。 只有 Azure AD 中的全局管理员或用户管理员可以创建、更新用户或删除现有用户。 如果你未充当其中的角色之一，必须让管理员为你创建新用户或者将你添加到这些角色之一。 [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2. 若要创建新用户，请确保用户名唯一，并且该用户位于本地 AD 中未联合到 Azure AD 的域内。 用户名必须在整个 Azure AD 中保持唯一。 不能在其域名与 Azure AD 联合的云中添加用户。
3. 若要更新用户，请确保不要更新已从本地 AD 同步的属性。 如果该用户已同步（即，如果源 =“Windows Server AD”），则在 Azure AD 中可以管理的属性仅包括“设置”和“身份验证联系人信息”部分中的属性。 若要更改其他任何属性，请在本地目录中更改。 下一次运行同步后，可在云中看到更新的属性。
4. 若要删除某个用户，请确保未从本地 AD 同步该用户。 如果该用户已同步（即，如果源 =“Windows Server AD”），请在本地目录中删除该用户。 运行同步后，可以看到该用户已从 Azure AD 中删除。

## <a name="recommended-documents"></a>**建议的文档**

* [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) 
* [使用 Azure 门户在 Azure AD 中创建新用户](https://docs.microsoft.com/azure/active-directory/active-directory-users-create-azure-portal) 
* [使用 Azure 门户在 Azure AD 中删除用户](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal) 
* [使用 Azure AD PowerShell 管理用户](https://docs.microsoft.com/powershell/azuread/v2/azureactivedirectory#users)


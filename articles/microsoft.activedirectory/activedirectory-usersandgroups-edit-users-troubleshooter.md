<properties 
    pageTitle="I can’t update the properties of a user in my directory"
    description=" 无法在目录中更新用户的属性"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder="2520"
    selfHelpType="resource"
    resourceTags="userandgroups_overview,userandgroups_user"
    cloudEnvironments="public"
    />



# <a name="i-cant-update-the-properties-of-a-user-in-my-directory"></a>无法在目录中更新用户的属性 

## <a name="recommended-steps"></a>**建议的步骤**
1.    确保你有权更新用户属性。 只有 Azure AD 的全局管理员或用户管理员可以更新用户属性。 如果你未充当其中的角色之一，必须让管理员为你更新用户属性或者将你添加到这些角色之一。 [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
2.    确保不要更新已从本地 AD 同步的属性。 如果该用户已同步（即，如果源 =“Windows Server AD”），则在 Azure AD 中可以管理的属性仅包括“设置”和“身份验证联系人信息”部分中的属性。 若要更改其他任何属性，请在本地目录中更改。 下一次运行同步后，可在云中看到更新的属性。

## <a name="recommended-documents"></a>**建议的文档**

* [使用 Azure 门户更改用户的配置文件信息](https://docs.microsoft.com/azure/active-directory/active-directory-users-profile-azure-portal) 
* [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles) 
* [使用 PowerShell 更新用户的配置文件属性](https://docs.microsoft.com/powershell/azuread/v2/set-azureaduser) 


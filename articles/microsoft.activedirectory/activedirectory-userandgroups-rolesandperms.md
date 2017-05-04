<properties
    pageTitle="Azure AD roles and permissions"
    description="Azure Active Directory 自助案例提交"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045782"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />


# <a name="azure-ad-roles-and-permissions"></a>Azure AD 角色和权限 
 
## <a name="recommended-steps"></a>**建议的步骤** 
1. 确保你已被分配到有权在 Azure AD 中管理角色的某个目录角色。 有权管理其他用户的角色的角色为“全局管理员”和“特权标识管理员”。 拥有某个 Azure 订阅的权限并不意味着拥有与该订阅关联的 Azure AD 租户的管理权限。 详细了解 [Azure AD 管理角色](https://docs.microsoft.com/azure/activedirectory/active-directory-assign-admin-roles)。
2. 分配对应于用户在 Azure AD 中所需权限的角色。 若要分配角色，请导航到用户的“目录角色”选项卡。 [了解每个 Azure AD 角色的权限](https://docs.microsoft.com/azure/activedirectory/active-directory-assign-admin-roles-azure-portal#administrator-permissions)。
3. 如果需要分配对某个 Azure 订阅或者订阅中某个资源（例如虚拟机）的访问权限，请导航到该 Azure 资源，然后在该位置分配访问权限。 分配有 Azure AD 角色并不意味着拥有 Azure 订阅资源的管理访问权限。 [在 Azure 门户中分配 Azure 资源访问权限](https://docs.microsoft.com/azure/activedirectory/role-based-access-control-configure#add-access)。

## <a name="recommended-documents"></a>**建议的文档** 
 
* [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directoryassign-admin-roles)
* [Azure 订阅与 Azure AD 的关系](https://docs.microsoft.com/azure/activedirectory/active-directory-how-subscriptions-associated-directory#how-an-azure-subscription-isrelated-to-azure-ad)
* [使用 PowerShell 将用户添加到 Azure AD 角色](https://docs.microsoft.com/powershell/azuread/v2/add-azureaddirectoryrolemember)
* [使用 PowerShell 管理对 Azure 订阅资源的访问权限](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-access-powershell) 

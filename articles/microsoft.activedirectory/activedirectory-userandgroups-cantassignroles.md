<properties
    pageTitle="I can’t assign roles to other users in the Azure AD tenant"
    description="Azure Active Directory 域疑难解答"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="4294"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview,userandgroups_user"
    productPesIds=""
    cloudEnvironments="public"
    />


# <a name="i-cant-assign-roles-to-other-users-in-the-azure-ad-tenant"></a>无法将角色分配到 Azure AD 租户中的其他用户

## <a name="recommended-steps"></a>**建议的步骤**
1. 确保你已被分配到有权在当前 Azure AD 中管理角色的某个目录角色。 如果你正在管理多个目录，请验证所访问的租户是否向全局管理员或特权标识管理员分配了权限。 在这种情况下，拥有某个 Azure 订阅的权限并不意味着拥有与该订阅关联的 Azure AD 的管理权限。 详细了解如何[分配 Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles-azure-portal)。
2. 分配对应于用户在 Azure AD 中所需权限的角色。 若要分配角色，请导航到用户的“目录角色”选项卡。 了解 [Azure AD 权限和角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles-azure-portal#administrator-permissions)。

## <a name="recommended-documents"></a>**建议的文档**

* [使用 PowerShell 将用户添加到 Azure AD 角色](https://docs.microsoft.com/powershell/azuread/v2/add-azureaddirectoryrolemember)
* [使用 PowerShell 管理对 Azure 订阅资源的访问权限](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-access-powershell)



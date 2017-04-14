<properties
    pageTitle="I can’t access an Azure subscription"
    description="Azure Active Directory 域疑难解答"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="4292"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview,userandgroups_user"
    productPesIds=""
    cloudEnvironments="public"
    />


# <a name="i-cant-access-an-azure-subscription"></a>无法访问 Azure 订阅

## <a name="recommended-steps"></a>**建议的步骤**

1. 如果你无法访问 Azure 订阅，请确保你在 Azure AD 中的角色有权管理租户，并且对该特定订阅拥有给定的权限。 如果需要分配对某个 Azure 订阅（例如虚拟机）的访问权限，请导航到该 Azure 资源，然后在该位置分配访问权限。 详细了解 [Azure AD 权限和角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles-azure-portal#administrator-permissions)。

2. 确保你对所要访问的 Azure 订阅拥有给定的权限，分配有 Azure AD 角色并不意味着自然而然拥有该 Azure AD 中的订阅的权限。  详细了解如何[分配对 Azure 资源的访问权限](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure#add-access)。

## <a name="recommended-documents"></a>**建议的文档**

* [使用 PowerShell 将用户添加到 Azure AD 角色](https://docs.microsoft.com/powershell/azuread/v2/add-azureaddirectoryrolemember)
* [使用 PowerShell 管理对 Azure 订阅资源的访问权限](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-access-powershell)



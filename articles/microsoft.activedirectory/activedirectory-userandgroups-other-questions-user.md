<properties 
    pageTitle="Other questions regarding user and group management"
    description="有关用户和组管理的其他问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    selfHelpType="generic"
    supportTopicIds="32565604"
    productPesIds="14785"
    cloudEnvironments="public"
 />
 

# <a name="other-questions-regarding-user-and-group-management"></a>有关用户和组管理的其他问题

## <a name="recommended-steps"></a>**建议的步骤**
1. 确保你已被分配到有权执行该操作的某个目录角色。 针对用户和组的大多数操作只能由全局管理员和用户管理员执行。 拥有某个 Azure 订阅的权限并不意味着拥有与该订阅关联的 Azure AD 的管理权限。 详细了解 [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)。
2. 若要尝试更新或者删除某个用户或组，请确保该用户或组未从本地 Active Directory 同步。 针对已同步的用户和组的大多数更改必须在本地目录中进行。 然后，需将这些更改同步到 Azure AD。
3. 若要为组定义高级动态成员身份规则，请确保该规则使用支持的语法。 详细了解[动态成员身份规则](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal)。

## <a name="recommended-documents"></a>**建议的文档**

* [Azure AD 管理角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)
* [Azure 订阅与 Azure AD 租户的关系](https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory#how-an-azure-subscription-is-related-to-azure-ad)
* [使用 Azure AD PowerShell 管理用户](https://docs.microsoft.com/powershell/azuread/v2/azureactivedirectory#users)
* [使用 Azure AD PowerShell 管理组](https://docs.microsoft.com/powershell/azuread/v2/azureactivedirectory#groups)



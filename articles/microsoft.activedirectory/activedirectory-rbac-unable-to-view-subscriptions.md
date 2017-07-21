<properties 
    pageTitle="I can’t add or manage resources in my directory"
    description="无法添加或管理我的目录中的资源"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jeffsta-MSFT"
    displayOrder="2524"
    selfHelpType="resource"
    resourceTags="directory_overview"
    cloudEnvironments="public"
    />


# <a name="unable-to-view-subscriptions-in-the-azure-portal"></a>无法在 Azure 门户中查看订阅

## <a name="recommended-steps"></a>**建议的步骤**

**验证你要登录到的帐户是否是与订阅相关联的帐户。** 如果你有 Azure AD 帐户和 Microsoft 帐户，则可能在登录时使用的是个人帐户而不是工作或学校帐户。 如果是这种情况，请登录到所需的帐户，并考虑[重命名个人帐户](https://support.microsoft.com/help/11545/microsoft-account-rename-your-personal-account)。

**验证你是否具有查看订阅的相应权限。**

1.  使用目录全局管理员的帐户登录到 Azure AD。
2.  选择“用户和组”，然后选择“所有用户”或“所有组”。
3.  搜索用户，然后打开用户边栏选项卡。
4.  在用户边栏选项卡上，选择“Azure 资源”。 将列出该用户的所有访问权限分配。 
5.  确认你有足够的权限查看订阅。 如果权限不足，请联系 IT 管理员以获得权限。 

**验证你在 Azure 门户中查看的目录是否是正确的目录。**

可能会在 Azure 门户中选择错误的目录。 

1.  若要确认，请在 Azure 门户的右上角选择你的用户配置文件。
2.  验证所在的目录是否是正确的目录。 如果不是，请切换到所需的目录。 

## <a name="recommended-documents"></a>**建议的文档**
* [按用户管理访问权限分配](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-assignments)
* [按资源管理访问权限分配](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure)
* [Azure RBAC 的内置角色](https://docs.microsoft.com/azure/active-directory/role-based-access-built-in-roles)


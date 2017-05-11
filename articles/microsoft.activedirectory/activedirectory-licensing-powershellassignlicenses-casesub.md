<properties 
    pageTitle="I can't assign licenses to a user or group"
    description="无法将许可证分配给用户或组"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1770"
    supportTopicIds="32570960"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
 />


# <a name="i-cant-assign-licenses-to-a-user-or-group"></a>无法将许可证分配给用户或组

## <a name="recommended-steps"></a>**建议的步骤**

若要管理用户许可证，必须使用具有以下所需[管理员角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)之一的帐户：全局管理员或用户管理员。 可在用户边栏选项卡上的“目录角色”选项卡中查看用户的角色。

下面是有关诊断许可证分配问题的一些有用提示：

1. 如果使用 Azure 门户分配许可证失败，请选择右上角显示的通知。 这会打开一个边栏选项卡，其中显示了有关错误的详细信息，包括此处所列的常见问题。

2. 在将许可证分配给某个用户之前，必须为该用户设置“使用位置”属性。 查看用户边栏选项卡上的“配置文件”属性可确认是否为用户设置了该属性。

3. 确保要分配的产品有足够的可用许可证。 可通过 Azure 门户中的[“Azure Active Directory”-&gt;“许可证”-&gt;“所有产品”](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products)查看可用许可证的数量。

4. 用户现有的另一个许可证所涵盖的服务可能与尝试分配的新许可证中的服务相冲突。 例如，如果用户已启用“Exchange Online (计划 1)”服务，则你无法分配包含“Exchange Online (计划 2)”的许可证。 必须禁用某个服务才能分配新许可证。 如果使用 Azure 门户或 PowerShell cmdlet，问题详细信息页将列出导致冲突的特定服务。

5. 如果尝试删除某个许可证但该操作失败，原因可能是用户的其他许可证包含的服务依赖于所要删除的服务。 如果使用 Azure 门户或 PowerShell cmdlet，问题详细信息页将列出存在依赖关系的特定服务。

6. 如果尝试将许可证分配到分配窗格中未列出的组，请注意，[基于组的许可](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal)目前以公共预览版提供，仅适用于具有 Azure AD Basic 或更高版本许可证的租户。



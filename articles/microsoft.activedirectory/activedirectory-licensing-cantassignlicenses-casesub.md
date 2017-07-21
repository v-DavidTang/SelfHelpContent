<properties
    pageTitle="I can't assign licenses to a user"
    description="无法将许可证分配到用户"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1770"
    supportTopicIds="32570959"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
 />


# <a name="i-cant-assign-licenses-to-a-user"></a>无法将许可证分配到用户

**首先要检查的项目**
1. 若要管理用户许可证，必须使用具有以下所需[管理员角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)之一的帐户：全局管理员或用户管理员。 可在用户边栏选项卡上的“目录角色”选项卡中查看用户的角色。

2. 如果使用 Azure 门户分配许可证失败，请务必单击右上角显示的通知。 这会打开一个边栏选项卡，其中显示了有关问题的详细信息。 在大多数情况下，参考这些信息就足以了解和解决问题。

## <a name="recommended-steps"></a>**建议的步骤**

1. 在将许可证分配给某个用户之前，必须为该用户设置“使用位置”属性。 查看用户边栏选项卡上的“配置文件”选项卡可确认是否为用户设置了该属性。

2. 确保要分配的产品有足够的可用许可证。 可通过 Azure 门户中的[“Azure Active Directory”-&gt;“许可证”-&gt;“所有产品”](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products)查看可用许可证的数量。

3. 用户现有的另一个许可证所涵盖的服务可能与尝试分配的新许可证中的服务相冲突。 例如，如果用户已启用“Exchange Online (计划 1)”服务，则你无法分配包含“Exchange Online (计划 2)”的许可证。 必须禁用某个服务才能分配新许可证。 如果使用 Azure 门户或 PowerShell cmdlet，问题详细信息页将列出导致冲突的特定服务。

4. 如果尝试删除某个许可证但该操作失败，原因可能是用户的其他许可证包含的服务依赖于所要删除的服务。 如果使用 Azure 门户或 PowerShell cmdlet，错误消息将列出存在依赖关系的特定服务。

5. 如果使用的是 Exchange Online，可能会使用相同的代理地址值错误地配置租户中的某些用户。 在这种情况下，许可证操作失败时可能会出现常规错误消息。 [这篇文章](https://support.microsoft.com/help/3042584/-proxy-address-address-is-already-being-used-error-message-in-exchange-online)包含有关此问题的详细信息，其中包括有关[如何使用远程 PowerShell 连接到 Exchange Online](https://technet.microsoft.com/library/jj984289.aspx) 的信息。

  若要识别租户中的哪些用户包含相同的代理地址，请执行以下 Exchange Online cmdlet：
```
Run Get-Recipient | where {$_.EmailAddresses -match <user principal name>} | fL Name, RecipientType,emailaddresses
```

6. 若要了解为何添加/删除了用户的许可证（例如，组织中的其他哪个人可能做了更改），请务必查看[审核日志](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit)。 将筛选器设置为许可证活动会显示所有修改，包括执行修改的“参与者”。


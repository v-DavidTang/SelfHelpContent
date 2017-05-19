 <properties 
    pageTitle="A user doesn't have the right licenses"
    description="用户没有适当的许可证"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1771"
    supportTopicIds=""
    selfHelpType="resource"
    resourceTags="licensing_overview"
    productPesIds=""
    cloudEnvironments="public"
 />


# <a name="a-user-doesnt-have-the-right-licenses"></a>用户没有适当的许可证

用户的“许可证”边栏选项卡上提供了有关该用户的许可证及其状态的完整信息。 如果未看到所需的许可证，请尝试遵循以下一条或两条提示。

1. 如果使用基于组的许可将许可证分配给用户，系统可能无法分配许可证。 用户的“许可证”选项卡上会显示此信息。 请参阅 docs.microsoft.com 上有关[识别和解决基于组的许可问题](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-problem-resolution-azure-portal)的文章。

2. 检查该许可证是否未其他管理员或租户中的进程删除。 可以在 [审核日志](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit) 边栏选项卡上查看租户中发生的许可证更改历史记录。 可以通过搜索 UPN（例如 joe@contoso.com）来查看最近是否删除了某个许可证。 此外，还可以[阅读有关 Azure AD 审核日志的详细信息](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-audit-events)。




<properties 
    pageTitle="A user doesn't have the right licensese"
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

用户的“许可证”边栏选项卡上提供了有关该用户的许可证及其状态的完整信息。 如果未看到所需的许可证，请考虑以下因素：

1. 如果使用基于组的许可将许可证分配给用户，系统可能无法分配许可证。 用户的“许可证”选项卡上会显示此信息。 请参阅 [docs.microsoft.com](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-problem-resolution-azure-portal) 上有关识别和解决基于组的许可问题的文章。

2. 检查该许可证是否未其他管理员或租户中的进程删除。 可以在“审核日志”边栏选项卡上查看租户中发生的许可证更改历史记录。[](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit)
  可以通过搜索 UPN（例如 <joe@contoso.com>）来查看最近是否删除了某个许可证。 可阅读 [此文](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-audit-events)，了解有关 Azure AD 审核日志的详细信息。




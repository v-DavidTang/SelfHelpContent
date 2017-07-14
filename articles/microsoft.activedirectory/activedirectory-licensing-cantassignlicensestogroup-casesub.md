<properties
    pageTitle="I can't assign licenses to a group"
    description="无法将许可证分配到组"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1770"
    supportTopicIds="32570958"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
 />


# 无法将许可证分配到组
<a id="i-cant-assign-licenses-to-a-group" class="xliff"></a>

**首先要检查的项目**
1. 若要管理组中的许可证，必须使用具有以下所需[管理员角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)之一的帐户：全局管理员或用户管理员。 可在用户边栏选项卡上的“目录角色”选项卡中查看用户的角色。

2. 如果使用 Azure 门户分配许可证失败，请务必单击右上角显示的通知。 这会打开一个边栏选项卡，其中显示了有关问题的详细信息。 在大多数情况下，参考这些信息就足以了解和解决问题。

3. 将许可证分配到组的功能目前以[预览版](https://blogs.technet.microsoft.com/enterprisemobility/2017/02/22/announcing-the-public-preview-of-azure-ad-group-based-license-management-for-office-365-and-more/)提供；可在[此文](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-advanced#limitations-and-known-issues)中详细了解限制和已知问题。 在使用预览版期间，需要 Azure AD Basic（或更高版本）的有效订阅 - 请在 Azure 门户中转到[许可证/所有产品](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products)检查是否有所需的订阅。

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>
1. 如果无法将许可证分配到某个组，请检查该组是否为“安全组”。 目前不支持 Office 365 组和通讯组。

2. 在组中分配或修改许可证时，可能需要在一段时间后才能向用户反映更改。 若要[确认许可证处理状态](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal#step-2-verify-that-the-initial-assignment-has-completed)，请查看组的“许可证”选项卡。

3. [在某些情况下](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-problem-resolution-azure-portal)，无法分配或删除用户的许可证。 调查某个用户相关的问题时，请务必转到该用户的“许可证”选项卡查看有关用户状态的完整信息；在大多数情况下，参考这些信息就足以了解和解决问题。

4. 若要了解为何添加/删除了用户或组的许可证（例如，组织中的其他哪个人可能做了更改），请务必查看[审核日志](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit)。 将筛选器设置为许可证活动会显示所有修改，包括执行修改的“参与者”。

5. 目前，PowerShell 对基于组的许可的支持受到限制，但某些功能已通过 PowerShell v1.0 cmdlet 公开。 [参阅此处的示例](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-ps-examples)。


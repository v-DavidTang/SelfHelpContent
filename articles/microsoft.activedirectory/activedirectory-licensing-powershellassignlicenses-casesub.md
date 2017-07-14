<properties
    pageTitle="Issues managing licenses using PowerShell"
    description="使用 PowerShell 管理许可证时出现问题"
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


# 使用 PowerShell 管理许可证时出现问题
<a id="issues-managing-licenses-using-powershell" class="xliff"></a>

**首先要检查的项目**
1. 问题是与基于用户的订阅（例如 Office 365、企业移动性 + 安全性、Dynamics 365 等）还是与 Azure 资源订阅（例如虚拟机、存储帐户）相关？ 对于 Azure 资源订阅问题，请务必在“订阅问题”下面开具支持票证。

2. Azure AD 有两个可以用来管理许可证的 PowerShell cmdlet 版本：
  * V2.0 包含 [Set-AzureADUserLicense](https://docs.microsoft.com/powershell/module/azuread/set-azureaduserlicense) 和 [Get-AzureADUserLicenseDetail](https://docs.microsoft.com/powershell/module/azuread/get-azureaduserlicensedetail) 等 cmdlet。
  * V1.0 包含 [Set-MsolUserLicense](https://docs.microsoft.com/powershell/module/msonline/Set-MsolUserLicense) 和 [Get-MsolUser](https://docs.microsoft.com/powershell/module/msonline/Get-MsolUser) 等 cmdlet。
  * 在[此处](https://technet.microsoft.com/library/dn771770.aspx)可以找到有关使用 PowerShell v1.0 管理 Office 365 许可证的有用示例。

3. 目前，PowerShell 对[基于组的许可](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal)的支持受到限制，但某些功能已通过 PowerShell v1.0 cmdlet 公开。 [参阅此处的示例](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-ps-examples)。

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>

1. 在某些情况下，由于已向用户分配了现有的许可证，许可证操作可能失败。 调查某个用户相关的问题时，请在 Azure 门户中打开该用户的边栏选项卡并选择“许可证”选项卡，其中包含有关该用户的状态的完整信息，显示当前分配的所有许可证（包括从组继承的许可证）。

2. 如果在租户中使用[基于组的许可](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal)，请注意，[无法直接删除或修改用户的继承许可证](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-advanced#direct-licenses-coexist-with-group-licenses)。 如果删除许可证或禁用许可证上的服务计划时出错，请查看用户的“许可证”选项卡，检查该用户是否没有继承的许可证。

3. 若要了解为何添加/删除了用户或组的许可证（例如，组织中的其他哪个人可能做了更改），请务必查看[审核日志](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit)。 将筛选器设置为许可证活动会显示所有修改，包括执行修改的“参与者”。

4. 如果使用的是 Exchange Online，可能会使用相同的代理地址值错误地配置租户中的某些用户。 在这种情况下，许可证操作失败时可能会出现常规错误消息。 [此文](https://support.microsoft.com/help/3042584/-proxy-address-address-is-already-being-used-error-message-in-exchange-online)包含有关此问题的详细信息。

  若要识别租户中的哪些用户包含相同的代理地址，请执行以下 Azure AD PowerShell cmdlet：
```
Get-AzureAdUser -All | Where {$_.ProxyAddresses -match <proxy address>} | Format-List ObjectId,UserPrincipalName,ProxyAddresses
```


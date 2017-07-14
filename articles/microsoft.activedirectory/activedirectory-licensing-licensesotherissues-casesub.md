<properties
    pageTitle="Other issues with licenses"
    description="其他许可证问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1770"
    supportTopicIds="32570962"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
 />


# 其他许可证问题
<a id="other-issues-with-licenses" class="xliff"></a>

**首先要检查的项目**
1. 问题是与基于用户的订阅（例如 Office 365、企业移动性 + 安全性、Dynamics 365 等）还是与 Azure 资源订阅（例如虚拟机、存储帐户）相关？ 对于 Azure 资源订阅问题，请务必在“订阅问题”下面开具支持票证。

2. 若要管理组中的许可证，必须使用具有以下所需[管理员角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)之一的帐户：全局管理员或用户管理员。 可在用户边栏选项卡上的“目录角色”选项卡中查看用户的角色。

3. 如果使用 Azure 门户分配许可证失败，请务必单击右上角显示的通知。 这会打开一个边栏选项卡，其中显示了有关问题的详细信息。 在大多数情况下，参考这些信息就足以了解和解决问题。

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>

1. 如果使用 [Azure 经典门户](https://manage.windowsazure.com/)时出现问题（例如，由于缺少 Azure 资源订阅，因此无法访问该门户），请考虑使用新式 [Azure 门户](https://portal.azure.com/)：它提供高级许可证管理功能，并且不需要 Azure 资源订阅即可访问。

2. 如果你想要创建一份报告来描述如何向租户中的用户分配许可证，则需要使用 PowerShell 脚本来下载各项用户数据，并在本地对其进行处理。 可以使用 PowerShell 版本 1.0 中的 cmdlet（例如 [Get-MsolUser](https://docs.microsoft.com/powershell/module/msonline/get-msoluser?view=azureadps-1.0)），也可以使用版本 2.0 中的 cmdlet（例如 [Get-AzureADUserLicenseDetail](https://docs.microsoft.com/powershell/module/azuread/Get-AzureADUserLicenseDetail?view=azureadps-2.0)）。


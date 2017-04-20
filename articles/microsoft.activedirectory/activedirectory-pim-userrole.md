<properties
    pageTitle="Unable to manage role in a Microsoft Online Services portal after being assigned or activated"
    description="在某些 Microsoft Online Services 门户中，最近已分配到某个角色或激活了其角色的用户无法进行管理"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="billmath"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32462545"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="unable-to-manage-role-in-a-microsoft-online-services-portal-after-being-assigned-or-activated"></a>在 Microsoft Online Services 门户中无法管理已分配或激活的角色

在 Azure AD 中显示某个用户后，可以使用 Azure 门户、PowerShell 或图形 API 接口将该用户分配到安全管理员等 Azure AD 角色。  完成角色分配后，该用户自身随即可以使用该角色通过这些接口管理 Azure AD。 但是，可能需要经过一段时间的延迟后，该用户才能使用该角色在其他 Microsoft Online Services 中进行管理。  在其他服务，最近被分配某个角色的用户可能看不到管理门户，或者会收到“拒绝访问”消息。

## <a name="recommended-steps"></a>**建议的步骤**


1. 在 Azure AD 中验证用户的角色分配是否正确。  执行此验证的最简单方法是通过 PowerShell 对 Microsoft Online Services 使用 [Get-MsolUserRole](https://docs.microsoft.com/powershell/msonline/v1/get-msoluserrole) cmdlet，或者使用 Azure AD v2 PowerShell [Get-AzureADDirectoryRoleMember](https://docs.microsoft.com/powershell/azuread/v2/get-azureaddirectoryrolemember) cmdlet。  例如，此命令响应表明某个用户在 Azure AD 中目前具有两种管理角色分配。

```
PS> Get-MsolUserRole -UserPrincipalName user@cexample.onmicrosoft.com

ObjectId                               Name                             Description
--------                               ----                             -----------
62e90394-69f5-4237-9190-012177145e10   Company Administrator            Company Administrator role has full access ...
e8611ab8-c189-46e8-94e1-60213ab1f814   Privileged Role Administrator    Privileged Role Administrator has access to...
```
2. 如果该用户要在 Azure 门户中管理 Azure AD，请让其刷新网页的浏览器视图。 如果该用户要在 Office 365 门户中进行管理，请在经过短暂的延迟后，让该用户重新打开门户网页。  


## <a name="recommended-documents"></a>**建议的文档**
* [使用 Azure AD Privileged Identity Management 排查提升的权限问题](https://social.technet.microsoft.com/wiki/contents/articles/37568.troubleshooting-elevated-permissions-with-azure-ad-privileged-identity-management.aspx)<br>
* [Azure AD 中的管理员角色](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles)


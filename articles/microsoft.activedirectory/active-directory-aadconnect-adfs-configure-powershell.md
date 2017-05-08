<properties
    pageTitle="I have AD FS installed and want to create federation with Azure Active Directory using PowerShell"
    description="使用 PowerShell 创建与 Azure AD 的联合"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="billmath"
    displayOrder="3"
    selfHelpType="generic"
    supportTopicIds="32570968"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>




# <a name="i-have-ad-fs-installed-and-want-to-create-federation-with-azure-active-directory-using-powershell"></a>我已安装 AD FS，想要使用 PowerShell 来创建与 Azure Active Directory 的联合 

## <a name="recommended-steps"></a>**建议的步骤**

建议使用 Azure Active Directory Connect (Azure AD Connect) 在 Azure AD 与 AD FS 之间建立联合。 Azure AD Connect 可以自动执行所有与联合相关的任务。 可在此处详细了解可能的操作。 如果无法使用 Azure AD Connect 创建与 AD FS 的联合信任，可以使用 PowerShell 创建与 Azure AD 的联合信任。
先决条件 

### <a name="follow-the-guidelines-here-and-install-azure-powershell-on-ad-fs-server"></a>遵照此处的指导，在 AD FS 服务器上安装 Azure PowerShell。 
创建联合的步骤



1. 确定要与 Azure AD 联合的域集。 创建联合时，必须知道是否要将多个域与同一个 AD FS 相联合
2. 以管理员身份运行 Microsoft Azure Active Directory PowerShell
3. 使用 GA 凭据连接到 Microsoft Online Services：`Convert-MsolService`
4. 将 MSOL AD FS 上下文服务器设置为 AD FS 服务器（可选）：如果不是在 AD FS 主服务器上运行 PowerShell 模块，请将适当的 AD FS 主服务器设置为上下文服务器：`Set-MsolADFSConect -Computer <adfs_server.contoso.com>`
5. 现在，可将域从托管域转换为联合域。 如果只要联合一个域，则在创建信任时需要将 SupportMultipleDomain 标志设置为 false；否则需要将它设置为 true：`Convert-MsoldomainToFederated -DomainName contoso.com -SupportMultipleDomain <$false/$true>`


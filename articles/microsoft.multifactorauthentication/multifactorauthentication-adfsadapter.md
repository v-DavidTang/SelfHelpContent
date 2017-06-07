<properties
    pageTitle="MFA Server (On-Premises)/Installing or configuring AD FS adapter"
    description="MFA 服务器（本地）/安装或配置 AD FS 适配器"
    service="microsoft.multifactorauthentication"
    resource=""
    authors="kgremban"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32336308"
    resourceTags=""
    productPesIds="14947"
    cloudEnvironments="public"
/>


# <a name="installing-or-configuring-ad-fs-adapter"></a>安装或配置 AD FS 适配器

## <a name="recommended-steps"></a>**建议的步骤**

如果在 ADFS 所在的同一台服务器上安装 Azure 多重身份验证服务器，则不需要使用适配器。 如果在另一台计算机上安装了 MFA 服务器，请执行以下步骤安装 ADFS 适配器：

1.    在所有 ADFS 服务器上安装 ADFS 适配器。 
2.    如果要在多台服务器上安装适配器，请只在主 ADFS 服务器上注册该适配器（使用文档中所述的 PowerShell 脚本）。 重新启动所有 ADFS 服务器，使注册生效。 
3.    确保在 MFA 服务器上安装 Web 服务 SDK。 Web 服务 SDK 是一个 IIS 组件。 需要在安装 Web 服务 SDK 之前安装 IIS。 
4.    如果安装 ADFS 适配器时遇到问题，请确保已安装 KB2919355 和.Net Framework 4.x。 
5.    在 <C:\Program files\Multi-Factor Authentication server> 中可以找到 ADFS 适配器的 MSI 安装程序。 文件名为 MultifactorAuthenticationAdfsAdapterSetup64.msi。 
6.    检查 ADFS OS 的版本。 该适配器适用于 Windows server 2012 R2 和更高版本。 对于早期的 OS，需要在 ADFS 计算机上安装 MFA 服务器，并将 MFA 与 IIS 身份验证相集成。 


## <a name="recommended-documents"></a>**建议的文档**
- [将 Azure 多重身份验证服务器配置为与 Windows Server 2012 R2 中的 AD FS 配合使用](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-w2k12)  
- [将 Azure 多重身份验证服务器配置为与 AD FS 2.0 配合使用](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-adfs2)  
- [升级 MFA 服务器的 AD FS 适配器](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-server-upgrade#upgrade-the-ad-fs-adapters) 



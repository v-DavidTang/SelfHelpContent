<properties
    pageTitle="MFA Server (On-Premises)/Other questions regarding MFA server (on-premises)"
    description="MFA 服务器（本地）/有关 MFA 服务器（本地）的其他问题"
    service="microsoft.multifactorauthentication"
    resource="Microsoft_AAD_IAM"
    authors="yossib"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565585"
    resourceTags=""
    productPesIds="14947"
    cloudEnvironments="public"
/>


# <a name="other-questions-regarding-mfa-server-on-premises"></a>有关 MFA 服务器（本地）的其他问题

## <a name="recommended-steps"></a>**建议的步骤**

如果创建 MFA 提供程序时遇到问题，请确认是否需要此类提供程序， 大多数情况下并不需要。 Azure 多重身份验证提供程序适用于没有 Azure MFA、Azure AD Premium 或 EMS 许可证，但仍想要利用完整版 Azure MFA 提供的功能的用户。 如果你有这些许可证，其中默认包含完整版 Azure MFA，则不需要 MFA 提供程序。 

如果在将用户从 Active Directory 同步到 MFA 服务器时遇到问题，请使用以下步骤：

1. 在 MultiFactorAuthSvc.log 和 MultiFactorAuthAdSyncScv.log 中检查错误。 
2. 在运行 AD 同步服务的 MFA 服务器上检查“目录集成”设置。 如果已选择“使用特定 LDAP 目录”，请确保绑定用户名/DN 和绑定密码正确。 可“测试”按钮验证这些凭据。 
3. 确保未选中“使用属性范围查询”。 不需要此选项，选中它可能会导致问题。 
4. 转到“同步”选项卡，确保已选择“始终执行完全同步”。 不建议使用增量同步。

## <a name="recommended-documents"></a>**建议的文档**

[Azure 多重身份验证服务器入门](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server)  
[Azure 多重身份验证提供程序入门](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-auth-provider)  
[LDAP 身份验证和 Azure 多重身份验证服务器](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-LDAP)  
[升级到最新的 Azure 多重身份验证服务器](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-server-upgrade)  


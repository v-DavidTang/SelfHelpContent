<properties
    pageTitle="Cannot start Azure AD Connect Synchronization Service"
    description="无法启动 Azure AD Connect 同步服务"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="223"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="cannot-start-azure-ad-connect-synchronization-service"></a>无法启动 Azure AD Connect 同步服务

## <a name="recommended-steps"></a>**建议的步骤**
无法在 Windows 服务控制管理器中启动同步服务。 常见的根本原因包括：

* 由同步服务用作安全上下文的 Azure AD Connect 同步服务帐户的密码最近已更改。 若要解决此问题，请参阅[更改 Azure AD Connect 同步服务帐户密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)一文。

* 未向 Azure AD Connect 同步服务帐户授予“作为服务登录”权限。 有关如何授予此权限的说明，请参阅[向帐户添加“作为服务登录”权限](https://technet.microsoft.com/library/cc794944(v=ws.10).aspx)一文。

* Azure AD Connect 服务器正在将 **LocalDB** 用作数据库，该数据库具有 10-GB 的空间限制。 如果使用 LocalDB，则达到此限制后，同步服务不再能正常启动或同步。 若要从此问题恢复，请遵循[Azure AD Connect：如何从 LocalDB 10-GB 限制恢复](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)一文中所述的步骤。

## <a name="recommended-documents"></a>**建议的文档**
* [更改 Azure AD Connect 同步服务帐户密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)  
* [Azure AD Connect：如何从 LocalDB 10-GB 限制恢复](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  


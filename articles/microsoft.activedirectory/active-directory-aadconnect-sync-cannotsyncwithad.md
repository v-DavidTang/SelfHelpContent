<properties
    pageTitle="Synchronization Service cannot import/export changes from on-premises AD"
    description="同步服务无法从本地 AD 导入/导出更改"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="225"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="synchronization-service-cannot-importexport-changes-from-on-premises-ad"></a>同步服务无法从本地 AD 导入/导出更改

## <a name="recommended-steps"></a>**建议的步骤**
常见的根本原因包括：

* 同步服务与本地 AD 通信时所用的 AD DS 服务帐户已被删除、其密码已更改或者其 userPrincipalName 已更改。 若要解决此问题，请参阅[更改 AD DS 帐户密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-addsacct-pass)一文。

* Azure AD Connect 服务器与 Azure AD 之间存在网络连接问题。 若要排查连接问题，请参阅[使用 Azure AD Connect 排查连接问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity)一文。

## <a name="recommended-documents"></a>**建议的文档**
* [更改 AD DS 帐户密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-addsacct-pass)   
* [使用 Azure AD Connect 排查连接问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity)  


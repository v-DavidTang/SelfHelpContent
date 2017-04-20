<properties
    pageTitle="Synchronization Service cannot import/export changes from Azure AD"
    description="同步服务无法从 Azure AD 导入/导出更改"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="226"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="synchronization-service-cannot-importexport-changes-from-azure-ad"></a>同步服务无法从 Azure AD 导入/导出更改

## <a name="recommended-steps"></a>**建议的步骤**
常见的根本原因包括：

* 同步服务与 Azure AD 通信时所用的 Azure AD 服务帐户已被删除、其密码已更改或者其 userPrincipalName 已更改。 若要解决此问题，请参阅 [Azure AD Connect 同步：如何管理 Azure AD 服务帐户](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)一文。

* Azure AD Connect 服务器与 Azure AD 之间存在网络连接问题。 若要排查连接问题，请参阅[使用 Azure AD Connect 排查连接问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity)一文。

## <a name="recommended-documents"></a>**建议的文档**
* [Azure AD Connect 同步：如何管理 Azure AD 服务帐户](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)  
* [使用 Azure AD Connect 排查连接问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity)  


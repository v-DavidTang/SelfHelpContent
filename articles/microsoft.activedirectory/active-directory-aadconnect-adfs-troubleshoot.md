<properties
    pageTitle="Synchronization Service cannot import/export changes from Azure AD"
    description="同步服务无法从 Azure AD 导入/导出更改"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="anandy"
    displayOrder="231"
    selfHelpType="generic"
    supportTopicIds="32565603"
    resourceTags="directory_overview, directory_ad_connect"
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="i-have-trouble-configuring--managing-federation-with-ad-fs"></a>配置/管理与 AD FS 的联合时遇到问题

## <a name="recommended-steps"></a>**建议的步骤**
Azure AD Connect 提供简单的步骤来配置和维护联合。 有关可以使用 AAD Connect 执行的所有联合相关任务，请参阅 [Azure AD Connect 和联合](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectfed-whatis)。 下面列出了一些常见问题和解决方法：

1. 使用备用登录 ID（除本地 userPrincipalName 属性以外的用户主体名称）的用户无法进行身份验证。
使用备用登录 ID 进行身份验证失败的最常见原因是颁发声明规则错误。 最新版本的 Azure AD Connect 可以帮助使用 AD FS 场中的必备配置来配置与备用登录 ID 的联合。 了解[详细信息](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#federate-with-azure-ad-using-alternateid-a-namealternateida)。

2. 如何使用 AAD Connect 将另一个域与 AD FS 联合？
可以使用 Azure AD Connect 中的“添加其他 Azure AD 域”任务将多个域与 AD FS 联合。 了解[详细信息](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#add-a-federated-domain-a-nameaddfeddomaina)。

3. 用户收到错误“请求的联合领域对象不存在”。
如果 AD FS 颁发的 issuerID 声明不正确，Azure AD 通常会引发此错误。 在某些旧版 Azure AD Connect 中，多个域联合方案中的颁发声明未正确设置。 升级到最新的 Azure AD Connect 可能会解决该问题。

## <a name="recommended-documents"></a>**建议的文档**
[Azure AD Connect 和联合身份验证](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectfed-whatis)  


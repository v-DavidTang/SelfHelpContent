<properties
    pageTitle="How to migrate Azure AD Connect from LocalDB to full SQL"
    description="如何将 Azure AD Connect 从 LocalDB 迁移到 SQL 完整版"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="2221"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="how-to-migrate-azure-ad-connect-from-localdb-to-full-sql"></a>如何将 Azure AD Connect 从 LocalDB 迁移到 SQL 完整版

## <a name="recommended-steps"></a>**建议的步骤**
不能直接将现有 Azure AD Connect 部署的 LocalDB 替换为完整版 SQL 的数据库， 而必须使用完整版 SQL 来部署新的 Azure AD Connect 服务器。 建议执行交叉迁移，将新的 Azure AD Connect 服务器（装有 SQL DB）部署为过渡服务器，与现有的 Azure AD Connect 服务器（装有 LocalDB）并存。 

* 有关如何使用 Azure AD Connect 配置远程 SQL 的说明，请参阅 [Azure AD Connect 的自定义安装](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom)一文。

* 有关如何通过交叉迁移进行 Azure AD Connect 升级的说明，请参阅 [Azure AD Connect：从旧版升级到最新版本](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-upgrade-previous-version#swing-migration)一文。

## <a name="recommended-documents"></a>**建议的文档**
* [Azure AD Connect：如何从 LocalDB 10-GB 限制恢复](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  
* [Azure AD Connect：从旧版升级到最新版本](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-upgrade-previous-version#swing-migration)  
* [Azure AD Connect 的自定义安装](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom)  


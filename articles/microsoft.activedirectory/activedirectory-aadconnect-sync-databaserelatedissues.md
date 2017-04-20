<properties
    pageTitle="Synchronizing AD to Azure AD/SQL-related installation and sync issues"
    description="将 AD 同步到 Azure AD/与 SQL 相关的安装和同步问题"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565592"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="synchronizing-ad-to-azure-adsql-related-installation-and-sync-issues"></a>将 AD 同步到 Azure AD/与 SQL 相关的安装和同步问题

## <a name="recommended-steps"></a>**建议的步骤**
1. 如果你将 **LocalDB** 用作 Azure AD Connect 的数据库并且已达到该数据库的 **10-GB 限制**，同步服务不再能正常工作。 可以删除运行历史记录数据以回收数据库空间，从而暂时恢复该服务。 有关详细信息，请参阅 [Azure AD Connect：如何从 LocalDB 10-GB 限制恢复](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)一文。

2. 如果想要使用完整 SQL 版本升级现有 Azure AD Connect 部署的 LocalDB，必须使用完整 SQL 版本部署新的 Azure AD Connect 服务器。 建议执行交叉迁移，将新的 Azure AD Connect 服务器（装有 SQL DB）部署为过渡服务器，与现有的 Azure AD Connect 服务器（装有 LocalDB）并存。

## <a name="recommended-documents"></a>**建议的文档**
* [Azure AD Connect 的先决条件](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-prerequisites)  
* [Azure AD Connect：如何从 LocalDB 10-GB 限制恢复](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  


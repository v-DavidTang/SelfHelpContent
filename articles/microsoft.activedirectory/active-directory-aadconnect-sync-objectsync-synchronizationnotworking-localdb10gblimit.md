<properties
    pageTitle="Synchronization Service stops working after LocalDB reaches 10-GB limit"
    description="LocalDB 达到 10-GB 限制后，同步服务停止工作"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="2222"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="synchronization-service-stops-working-after-localdb-reaches-10-gb-limit"></a>LocalDB 达到 10-GB 限制后，同步服务停止工作

## <a name="recommended-steps"></a>**建议的步骤**
* Azure AD Connect 要求使用 SQL Server 数据库来存储标识数据。 可以使用随 Azure AD Connect 一起安装的默认 SQL Server 2012 Express LocalDB，也可以使用你自己的完整 SQL。 SQL Server Express 存在 10 GB 的大小限制。 使用 LocalDB 并达到此限制后，Azure AD Connect Synchronization Service 将无法正常启动或同步。

* 若要从此问题恢复，请遵循[Azure AD Connect：如何从 LocalDB 10-GB 限制恢复](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)一文中所述的步骤。


## <a name="recommended-documents"></a>**建议的文档**
* [Azure AD Connect：如何从 LocalDB 10-GB 限制恢复](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  


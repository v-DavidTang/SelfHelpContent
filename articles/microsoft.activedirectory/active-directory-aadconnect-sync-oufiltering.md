<properties
    pageTitle="Synchronization issue with OU-based filtering"
    description="使用基于 OU 的筛选进行同步的问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="222"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview, userandgroups_user, userandgroups_group"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="synchronization-issue-with-ou-based-organizational-unit-filtering"></a>使用基于 OU（组织单位）的筛选进行同步的问题

## <a name="recommended-steps"></a>**建议的步骤**
配置基于 OU 的筛选时要注意的重要事项：

* 设置基于 OU 的筛选后，必须根据[配置筛选 - 应用并验证更改](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-configure-filtering#apply-and-verify-changes)文章部分中所述，依次执行**完全导入**和**增量同步**。

* 默认情况下，将会同步配置基于 OU 的筛选之后创建的新 OU。 如果你不想要同步新 OU，请遵循[配置筛选 - 基于组织单位的筛选](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-configure-filtering#organizational-unitbased-filtering)文章部分中所述的配置步骤。

* 如果有多个信任的林，则应选择 **ForeignSecurityPrincipals** 容器。 使用此容器可以解析跨林安全组成员身份。

* 如果将**基于组的筛选**与基于 OU 的筛选结合使用，必须包含组和成员对象所在的 OU。

* 更改现有 OU 的名称可能会导致基于 OU 的筛选无法正常运行。 如果需要更改现有 OU 的名称，必须在 Azure AD Connect 服务器上重新配置基于 OU 的筛选。

## <a name="recommended-documents"></a>**建议的文档**
* [Azure AD Connect 同步：配置筛选 - 基于组织单位的筛选](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-configure-filtering#organizational-unitbased-filtering)  


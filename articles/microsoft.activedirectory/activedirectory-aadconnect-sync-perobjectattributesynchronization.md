<properties
    pageTitle="Synchronizing AD to Azure AD/Per object or attribute synchronization"
    description="将 AD 同步到 Azure AD/按对象或属性同步"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32570976"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="synchronizing-ad-to-azure-adper-object-or-attribute-synchronization"></a>将 AD 同步到 Azure AD/按对象或属性同步

## <a name="recommended-steps"></a>建议的步骤

**同步特定用户、组或联系人对象的问题**

如果同步特定的对象时遇到问题：

  * 检查对应于此对象的任何同步错误。 有关常见同步错误的详细信息，请参阅[排查同步过程中发生的错误](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-sync-errors)一文。 将通过以下方式向客户显示同步错误：
  
    * 通过 Azure AD Connect Health 的[对象级同步错误报告](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync)。 目前只会向选定的客户显示这些错误。
    
    * 标识同步错误报告 - 每当 Azure AD Connect 完成同步周期但出错时，就会向租户的技术通知联系人发送此电子邮件通知。
    
    * 通过[同步服务管理器的“操作”选项卡](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-service-manager-ui-operations)。
    
  * 在 [重复属性复原](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency) 功能下检查重复属性错误。

  * 如果未发现此对象的任何错误，请遵循[排查对象无法同步到 Azure AD 的问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-object-not-syncing)一文中所述的故障排除步骤。


**使用基于 OU（组织单位）的筛选进行同步的问题**

配置基于 OU 的筛选时要注意的重要事项：

  * 设置基于 OU 的筛选后，必须根据[配置筛选 - 应用并验证更改](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-configure-filtering#apply-and-verify-changes)文章部分中所述，依次执行**完全导入**和**增量同步**。

  * 默认情况下，将会同步配置基于 OU 的筛选之后创建的新 OU。 如果你不想要同步新 OU，请遵循[配置筛选 - 基于组织单位的筛选](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-configure-filtering#organizational-unitbased-filtering)文章部分中所述的配置步骤。

  * 如果有多个信任的林，则应选择 **ForeignSecurityPrincipals** 容器。 使用此容器可以解析跨林安全组成员身份。

  * 如果将**基于组的筛选**与基于 OU 的筛选结合使用，必须包含组和成员对象所在的 OU。

  * 重命名现有的 OU 可能会导致基于 OU 的筛选无法正常运行。 如果需要更改现有 OU 的名称，必须在 Azure AD Connect 服务器上重新配置基于 OU 的筛选。


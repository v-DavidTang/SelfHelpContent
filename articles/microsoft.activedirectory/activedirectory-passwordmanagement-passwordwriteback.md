<properties
    pageTitle="I'm having a problem with password writeback"
    description="密码重置/密码写回"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia, gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565598"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />


# <a name="im-having-a-problem-with-password-writeback"></a>我在使用密码写回时遇到问题

## <a name="recommended-steps"></a>**建议的步骤**

**配置密码写回时遇到问题**

* 密码写回是一项高级功能。

* 请务必了解许可要求：
  * 你在组织中必须至少分配有一个许可证
    * **仅限云用户** - 任何 Office 365 (O365) 付费 SKU 或 Azure AD Basic
    * **云和/或本地用户** - Azure AD Premium P1 或 P2、企业移动性 + 安全性 (EMS) 或 Secure Productive Enterprise (SPE)
    * 若要详细了解许可要求，请参阅 [Azure AD 自助密码重置的许可要求](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing)一文

* 至少拥有一个管理员帐户和一个测试用户帐户，并且拥有适当的许可证之一。

* 必须将 Azure AD Connect 连接到主域控制器模拟器，以便密码写回能够工作。 可以通过右键单击 Active Directory 同步连接器的“属性”，然后选择“配置目录分区”，将 Azure AD Connect 配置为使用主域控制器。 在这里，请查找“域控制器连接设置”部分，并检查标题为“仅使用首选的域控制器”的框。 *注意：如果首选的 DC 不是 PDC 模拟器，Azure AD Connect 将会访问 PDC 来执行密码写回。*

* 已在你的租户中配置和启用了密码重置。 有关详细信息，请参阅[让用户重置其 Azure AD 密码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)。

* 确保用于启用密码写回的管理员帐户是云管理员帐户（在 Azure AD 而不是本地 AD 中创建的帐户）

* 拥有运行 Windows Server 2008 R2、Windows Server 2012 或 Windows Server 2012 R2 并装有最新服务包的单林或多林 AD 本地部署。

* 已安装了 Azure AD 同步工具，并已准备好 AD 环境，可随时同步到云。 *测试密码写回之前，请确保完成完整导入，并在 Azure AD Connect 中从本地 AD 与 Azure AD 执行完全同步*。
  * 详细了解如何[在 Azure AD Connect 中执行完全同步和完全导入](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations#staging-mode)

**遇到密码写回连接问题**

1. 下载并启用最新版本的 [Azure AD Connect](https://www.microsoft.com/download/details.aspx?id=47594)
2. 防火墙配置：
   * Azure AD Connect 工具（1.1.443 和更高版本）需要以下网站的**出站 HTTPS** 访问权限：
     * passwordreset.microsoftonline.com
     * servicebus.windows.networks
   * 允许空闲连接保持至少 2-3 分钟。

**仍然遇到密码写回的问题**

如果仍然出现问题，请尝试在 Azure AD Connect 工具中禁用再重新启用密码写回服务。

* 详细了解如何[禁用再重新启用密码写回](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#disable-and-re-enable-the-password-writeback-feature)。

## <a name="recommended-documents"></a>**建议的文档**

* [排查密码写回问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [密码写回事件日志错误代码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [排查密码写回连接问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [常见问题解答 - 密码写回](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)


 <properties
    pageTitle="Password Management/Password Writeback"
    description="密码管理/密码写回"
    service="microsoft.aad"
    resource="activedirectory"
    authors="zhchia, gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565598"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="password-managementpassword-writeback"></a>密码管理/密码写回
## <a name="pre-requisites"></a>先决条件
* 确保租户具有有效的许可证，可以使用 Azure AD 自助密码重置：
    * Azure AD Premium 1
    * Azure AD Premium 2
    * 企业移动性 + 安全性 E3
    * 企业移动性 + 安全性 E5
    * Secure Productive Enterprise E3
    * Secure Productive Enterprise E5


* 你至少拥有一个管理员帐户和一个测试用户帐户，并且拥有上述许可证之一。

* 必须将 Azure AD Connect 连接到主域控制器模拟器，以便密码写回能够工作。 可以根据需要通过右键单击 Active Directory 同步连接器的“属性”，然后选择“配置目录分区”将 Azure AD Connect 配置为使用主域控制器。 在这里，请查找“域控制器连接设置”部分，并检查标题为“仅使用首选的域控制器”的框。 *注意：如果首选的 DC 不是 PDC 模拟器，Azure AD Connect 将会访问 PDC 来执行密码写回。*

* 已在你的租户中配置和启用了密码重置。 有关详细信息，请参阅[让用户重置其 Azure AD 密码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)。

* 确保用于启用密码写回的管理员帐户是云管理员帐户（在 Azure AD 而不是本地 AD 中创建的帐户）

* 拥有运行 Windows Server 2008 R2、Windows Server 2012 或 Windows Server 2012 R2 并装有最新服务包的单林或多林 AD 本地部署。

* 已安装了 Azure AD 同步工具，并已准备好 AD 环境，可随时同步到云。 *测试密码写回之前，请确保完成完整导入，并在 Azure AD Connect 中从本地 AD 与 Azure AD 执行完全同步*。

## <a name="recommended-steps"></a>**建议的步骤**
1. 下载最新版 Azure AD Connect [1.1.443.0](https://www.microsoft.com/download/details.aspx?id=47594)
2. 在 Azure AD Connect 中启用密码写回
3. 配置防火墙
    * Azure AD Connect 工具（1.1.443 和更高版本）需要以下网站的**出站 HTTPS** 访问权限：
        * passwordreset.microsoftonline.com
        * servicebus.windows.networks
4. 允许空闲连接保持至少 2-3 分钟。

\**如果仍然出现问题，请尝试在 Azure AD Connect 工具中禁用再重新启用该服务*


## <a name="recommended-documents"></a>**建议的文档**
* [从客户体验总结的重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [排查密码写回问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [密码写回事件日志错误代码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [排查密码写回连接问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [常见问题解答 - 密码写回](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)


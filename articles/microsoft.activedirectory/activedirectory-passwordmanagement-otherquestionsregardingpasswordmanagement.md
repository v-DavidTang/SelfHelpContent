<properties
    pageTitle="Other questions about password reset"
    description="密码重置/有关密码重置的其他问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565599"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />


# <a name="im-having-other-problems-with-password-reset"></a>重置密码时遇到其他问题

## <a name="recommended-steps"></a>**建议的步骤**

**遇到的密码重置问题并未包括在其他类别中**

* 请确保你有权重置密码。 *只有全局、密码和用户管理员可以重置用户密码。* 全局管理员还可以重置其他特权管理员的密码。

* 请务必了解许可要求：
  * 你在组织中必须至少分配有一个许可证
    * **仅限云用户** - 任何 Office 365 (O365) 付费 SKU 或 Azure AD Basic
    * **云和/或本地用户** - Azure AD Premium P1 或 P2、企业移动性 + 安全性 (EMS) 或 Secure Productive Enterprise (SPE)
    * 若要详细了解许可要求，请参阅 [Azure AD 自助密码重置的许可要求](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing)一文

**测试设置的密码重置策略时遇到问题**

* 最近应用的策略可能需要花费几分钟才能复制到所有数据中心和终结点。 与数据中心之间的实际距离也会影响应用更改的速度。

* 请使用最终用户而不是管理员的身份测试，试运行时使用少量的用户。 **在 Azure 门户中配置的策略仅适用于最终用户，而不适用于管理员。** Microsoft 对任何 Azure 管理员角色（示例：全局管理员、支持管理员、密码管理员等）强制实施强默认的**双重关口**密码重置策略
   * 详细了解[针对管理员的策略](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-policy#administrator-password-policy-differences)

**我想要部署密码重置，但不想要让用户注册其他安全信息**

* 为用户预先填充数据，这样，他们就不需要注册！
   * 在组织中推出密码重置之前，可以管理员的身份为用户设置电话和电子邮件属性。 可以使用 API、PowerShell 或 Azure AD Connect 实现此目的。 以下主题提供了详细信息：
     * [在无需用户注册的情况下部署密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data#set-and-read-authentication-data-using-powershell)
     * [密码重置使用哪些数据](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data)

**访问密码重置审核日志时遇到问题**

* 请确保你有权查看审核日志。 只为以下角色授权：
  * 全局管理员
  * 安全管理员
  * 安全读者

**我想要查看从最初部署后就开始生成的所有密码重置审核事件**

* 报告中最多会存储过去 30 天内生成的 120,000 个密码重置/注册事件。 下载 CSV 时，UI 中最多只能显示这么多事件。 使用 PowerShell 可以查看 100 万个事件。
* 使用以下链接了解详细信息：
  * [通过 Azure AD 报告和事件 API 查看自助密码重置事件](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-retrieve-password-management-events-from-the-azure-ad-reports-and-events-api)
  * [如何通过 PowerShell 快速下载密码重置注册事件](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-download-password-reset-registration-events-quickly-with-powershell)

**想要详细了解密码重置报告功能**

* 使用 Azure 门户中“用户和组”下面的 Azure AD 密码重置审核日志查看谁正在注册或重置密码
  * 有关更多详细信息，请访问以下链接：
    * [密码重置报告概述](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#overview-of-password-management-reports)
    * [如何在 Azure 门户中查看密码重置报告](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-view-password-management-reports)
    * [通过 Azure AD 报告和事件 API 查看自助密码重置事件](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-retrieve-password-management-events-from-the-azure-ad-reports-and-events-api)
    * [如何通过 PowerShell 快速下载密码重置注册事件](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-download-password-reset-registration-events-quickly-with-powershell)


## <a name="recommended-documents"></a>**建议的文档**

* [常见问题解答 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [故障排除 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)
* [入门 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [最佳做法 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [审核日志 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights)
* [密码策略 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-policy)
* [了解详细信息 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more)
* [密码重置工作原理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-how-it-works)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)


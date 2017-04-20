<properties
   pageTitle="Password Management/Other questions regarding password management"
   description="密码管理/有关密码管理的其他问题"
   service="microsoft.aad"
   resource="activedirectory"
   authors="gahug"
   displayOrder=""
   selfHelpType="generic"
   supportTopicIds="32565599"
   resourceTags=""
   productPesIds="14785"
   cloudEnvironments="public"
/>


# <a name="password-managementother-questions-regarding-password-management"></a>密码管理/有关密码管理的其他问题
## <a name="pre-requisites"></a>先决条件
* 确保租户具有有效的许可证，可以使用 Azure AD 自助密码重置：
    * Azure AD Premium 1
    * Azure AD Premium 2
    * 企业移动性 + 安全性 E3
    * 企业移动性 + 安全性 E5
    * Secure Productive Enterprise E3
    * Secure Productive Enterprise E5

## <a name="tips"></a>提示
* [测试](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-2-testing---test-with-an-end-user-not-an-administrator-and-pilot-with-a-small-set-of-users) - 使用最终用户而不是管理员的身份测试，试运行时使用少量的用户。 **在管理 UX 中配置的策略仅适用于最终用户，而不适用于管理员。** 为了确保组织的安全，Microsoft 针对管理员实施增强的默认密码重置策略。 <br>

* [部署](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-3-deployment---pre-populate-data-for-your-users-so-they-dont-have-to-register) - 为用户预先填充数据，这样用户就不需要注册！
在组织中推出密码重置之前，可以管理员的身份为用户设置电话和电子邮件属性。 可以使用 API、PowerShell 或 Azure AD Connect 实现此目的。 以下主题提供了详细信息：
  * [在无需用户注册的情况下部署密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#deploying-password-reset-without-requiring-end-user-registration)
  * [密码重置使用哪些数据](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#what-data-is-used-by-password-reset)


* [报告](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-7-reporting---see-who-is-registering-or-resetting-passwords-with-the-azure-ad-sspr-audit-logs) - 使用 Azure 门户中“用户和组”下面的 Azure AD 密码重置审核日志查看谁正在注册或重置密码 <br>
有关更多详细信息，请访问以下链接：
    * [密码管理报告概述](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#overview-of-password-management-reports)
    * [如何在 Azure 门户中查看密码管理报告](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-view-password-management-reports)
    * [通过 Azure AD 报告和事件 API 查看自助密码管理事件](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-retrieve-password-management-events-from-the-azure-ad-reports-and-events-api)
    * [如何通过 PowerShell 快速下载密码重置注册事件](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-download-password-reset-registration-events-quickly-with-powershell)


## <a name="recommended-documents"></a>**建议的文档**
* [从客户体验总结的重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [常见问题解答 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [故障排除 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)
* [入门 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [最佳做法 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [审核日志 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights)
* [密码策略 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-policy)
* [了解详细信息 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more)
* [密码管理的工作原理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-how-it-works)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)


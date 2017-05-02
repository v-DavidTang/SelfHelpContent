<properties
    pageTitle="Administrator-initiated password reset"
    description="密码管理/管理员启动的密码重置"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia, gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045781"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />


# <a name="administrator-initiated-password-reset"></a>管理员发起的密码重置

## <a name="recommended-steps"></a>**建议的步骤**
*  确保你有权执行此操作。 *只有全局、密码和用户管理员可以重置用户密码。* 全局管理员还可以重置其他特权管理员的密码。 如果你无权执行此任务，请向上述管理员之一求助，或者使用[自助密码重置服务](https://passwordreset.microsoftonline.com/)
* 确保租户具有有效的许可证，可以使用 Azure AD 自助密码重置：
    * Azure AD Premium 1
    * Azure AD Premium 2
    * 企业移动性 + 安全性 E3
    * 企业移动性 + 安全性 E5
    * Secure Productive Enterprise E3
    * Secure Productive Enterprise E5

有关 Azure AD 许可的最终规范（同时，始终是最新的信息源）在 [Azure Active Directory 定价页](https://azure.microsoft.com/pricing/details/active-directory/)上提供。

## <a name="recommended-steps"></a>**建议的步骤**
1. 使用用户所在目录的全局管理员帐户登录到 Azure 门户。
2. 选择“更多服务”，在文本框中输入“用户和组”，然后按 **Enter**。
3. 在“用户和组”边栏选项卡中，选择“用户”。
4. 在“用户和组 - 用户”边栏选项卡中，从列表中选择一个用户。
5. 在所选用户的边栏选项卡中，选择“概述”，然后在命令栏中选择“重置密码”。
6. 在“重置密码”边栏选项卡中选择“重置密码”，然后遵照屏幕说明操作。

*注意：Office 管理门户/O365 管理移动应用不支持密码写回*



## <a name="recommended-documents"></a>**建议的文档**
* [从客户体验总结的重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [密码管理入门](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
* [排查管理员发起的密码重置问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [常见问题解答 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)


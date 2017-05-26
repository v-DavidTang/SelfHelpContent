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


# <a name="im-having-problems-resetting-a-users-password"></a>重置用户的密码时遇到问题

## <a name="recommended-steps"></a>**建议的步骤**

**重置用户的密码时遇到问题**

* 请确保你有权重置密码。 *只有全局、密码和用户管理员可以重置用户密码。* 全局管理员还可以重置其他特权管理员的密码。

* 请务必了解许可要求：
  * 你在组织中必须至少分配有一个许可证
    * **仅限云用户** - 任何 Office 365 (O365) 付费 SKU 或 Azure AD Basic
    * **云和/或本地用户** - Azure AD Premium P1 或 P2、企业移动性 + 安全性 (EMS) 或 Secure Productive Enterprise (SPE)
    * 若要详细了解许可要求，请参阅 [Azure AD 自助密码重置的许可要求](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing)一文

* 若要重置用户的密码，请在 Azure AD 中找到该用户。 然后，在该用户的概述边栏选项卡中单击“重置密码”按钮

**密码重置按钮灰显**

* 你无权重置**此**用户的密码。 *只有全局、密码和用户管理员可以重置用户密码。* 全局管理员还可以重置其他特权管理员的密码。

**未看到密码重置边栏选项卡**

* 你无权重置密码。 *只有全局、密码和用户管理员可以重置用户密码。* 全局管理员还可以重置其他特权管理员的密码。

**在密码重置中未看到本地集成边栏选项卡**

* 本地集成边栏选项卡只出现在混合环境中 - 这意味着，要使用密码写回处理本地用户的密码。

* 在以下情况下，不会显示此边栏选项卡：
  * 未使用密码写回
  * 密码写回的安装/连接有问题
  * Azure AD Connect 的安装/连接有问题
  * 有关排查密码写回问题的详细步骤，请参阅[排查密码写回问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)部分

**不知道如何重置用户的密码**

1. 以相应管理员的身份登录到 Azure 门户。
2. 转到“用户和组”边栏选项卡，然后选择“所有用户”
3. 从列表中选择用户。
4. 对于选定的用户，请选择“概述”，然后在命令栏中选择“重置密码”。
5. 选择“重置密码”按钮，然后遵照屏幕说明操作。
   * 只有通过 **Azure 门户**执行的重置才支持密码写回。

**我已从 Office 365 管理门户或 Office 365 移动应用程序重置了某个本地用户的密码，但该用户仍然无法登录**

* 此门户不支持密码写回。 请 Azure 门户 ([portal.azure.com](https://portal.azure.com/)) 中再次重置该用户的密码

## <a name="recommended-documents"></a>**建议的文档**

* [密码重置入门](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
* [排查管理员发起的密码重置问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [常见问题解答 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)


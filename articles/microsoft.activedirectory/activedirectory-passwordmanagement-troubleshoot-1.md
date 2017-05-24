<properties
    pageTitle="Problems testing password reset policy"
    description="从客户体验总结的重要提示 - 提示 2"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="200"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public"
/>


# <a name="problems-testing-password-rest-policy"></a>测试密码重置策略时遇到问题

## <a name="recommended-steps"></a>**建议的步骤**
**我重置了密码，但使用的策略不是门户中设置的策略**
* 请使用最终用户而不是管理员的身份测试。

* 使用管理员身份测试时，我们会强制实施管理员密码重置策略（定义如下）。 这意味着，如果使用管理员身份测试，则看不到在 Azure 门户中配置的策略。

* 在 Azure 门户中配置的策略仅适用于最终用户。
* 为了确保提高组织的安全性，Microsoft 强制实施针对管理员的较强默认密码重置策略（该策略可能不同于你为最终用户设置的策略）。

**我想要了解管理员密码重置策略**
* **适用对象** - 任何管理员角色（全局管理员、支持管理员、密码管理员等）
* **单门策略适用条件...**
 * ...启动/创建试用版后前 30 天，**或**
 * ...虚域不存在**且** Azure AD Connect 没有同步标识
 * **_必需条件_**：“身份验证电子邮件”、“备用电子邮件”、“身份验证电话”、“移动电话”或“办公电话”中的任何**一个**有值存在
* **双门策略适用条件...**
 * ...前 30 天试用已过，**或**
 * ...虚域存在，**或**
 * ... 已允许 Azure AD Connect 从本地环境同步标识
 * _**必需条件**_：“身份验证电子邮件”、“备用电子邮件”、“身份验证电话”、“移动电话”或“办公电话”中的任何**两个**有值存在


## <a name="recommended-documents"></a>**建议的文档**

* [测试密码重置策略时遇到问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-2-testing---test-with-an-end-user-not-an-administrator-and-pilot-with-a-small-set-of-users)
* [从客户体验总结的重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [密码管理入门](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
* [常见问题解答 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [故障排除 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)


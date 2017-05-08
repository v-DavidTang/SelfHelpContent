<properties
    pageTitle="I tested password reset with an administrative role and don't see the policy enforced"
    description="从客户体验总结的重要提示 - 提示 2"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="200"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public"
/>


# <a name="i-tested-password-reset-with-an-administrative-role-and-dont-see-the-policy-enforced"></a>我已使用管理角色测试密码重置，但未看到策略被强制实施

## <a name="recommended-steps"></a>**建议的步骤**
使用管理员进行测试时，我们会强制实施管理员密码重置策略，该策略定义如下。 这意味着，对于此用户，你不会看到为自己的最终用户配置的策略的预期效果。

在 Azure 门户中配置的策略仅适用于最终用户，而不适用于管理员。 为了确保提高组织的安全性，Microsoft 强制实施针对管理员的较强默认密码重置策略（该策略可能不同于你为最终用户设置的策略）。

### <a name="administrator-password-reset-policy"></a>管理员密码重置策略
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

[在 DOCS.com 上查看](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-2-testing---test-with-an-end-user-not-an-administrator-and-pilot-with-a-small-set-of-users)

## <a name="recommended-documents"></a>**建议的文档**

* [从客户体验总结的重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [密码管理入门](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
* [常见问题解答 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [故障排除 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)


<properties
    pageTitle="I'm having a problem with self-service password reset"
    description="密码管理/自助式密码更改/重置"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045826"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />


# <a name="im-having-a-problem-with-self-service-password-reset"></a>我在使用自助密码重置时遇到问题
## <a name="recommended-steps"></a>**建议的步骤**
* 确保租户具有有效的许可证，可以使用 Azure AD 自助密码重置：
    * Azure AD Premium 1
    * Azure AD Premium 2
    * 企业移动性 + 安全性 E3
    * 企业移动性 + 安全性 E5
    * Secure Productive Enterprise E3
    * Secure Productive Enterprise E5

有关 Azure AD 许可的最终规范（同时，始终是最新的信息源）在 [Azure Active Directory 定价页](https://azure.microsoft.com/pricing/details/active-directory/)上提供。

## <a name="recommended-steps"></a>**建议的步骤**
1. 将用户定向到 [aka.ms/ssprsetup](https://login.microsoftonline.com/common/oauth2/authorize?client_id=0000000c-0000-0000-c000-000000000000&redirect_uri=https%3A%2F%2Faccount.activedirectory.windowsazure.com%2F&response_mode=form_post&response_type=code%20id_token&scope=openid%20profile&state=OpenIdConnect.AuthenticationProperties%3D02LGeV2aaOpBfeyrPlPTVE9v9W3rf0E_VtBiNcjuL12zhaz8BdJ613HFOdYPXhNva7OX8tUieWVS1ldrysmNHg-XCO7bW8Pe82sA4RnjWozG43QBmckgtxvqZvUaty0ZNhBtzMtrjG5qW1v06t4jCAd03c-h0opfkRABw4Y2cvKoYnQy0tfpyRsC1KI3DngNKzhbtPXIYKjxHw02Ld-9RgJVjNxRrMppzhE6EJsjbfD0PpnwbwLp-tMnT5M3hS60SJwZQjvjfocM-x2EcXJhPhG1lfbSGIoZi3yHh12qyVI&nonce=1491428196.4kvRPWtSmTOR_qzakP8WpQ&nux=1)，让他们为自助密码重置注册其他安全信息。
    * 你也可以使用 API、Powershell 或 Azure AD Connect 为用户预先填充数据（电子邮件和电话属性）。
    * 若要了解操作方法，请参阅：
        * [在无需用户注册的情况下部署密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#deploying-password-reset-without-requiring-end-user-registration)
        * [密码重置使用哪些数据](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#what-data-is-used-by-password-reset)
2. 为用户填充数据后（由用户自己填充或者由管理员填充），请将他们定向到 [aka.ms/sspr](https://passwordreset.microsoftonline.com/)，使其能够重置自己的密码。
3. 如果用户仍然遇到问题，很有可能用户是**联合**用户或**密码哈希同步**用户。 这意味着密码写回服务可能存在问题。
    * 若要快速解决写回问题，请查看[重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)中的[提示 5](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-5-writeback---look-at-the-application-event-log-on-your-aad-connect-machine-to-troubleshoot-password-writeback) 和[提示 6](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-6-writeback---ensure-you-enable-the-correct-permissions-firewall-rules-and-connection-settings-for-password-writeback)
    * 有关密码写回配置的详细信息，请参阅：
        * [如何让用户重置其 Azure AD 密码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
        * [如何让用户重置或更改其本地 Active Directory 密码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-or-change-their-ad-passwords)


## <a name="recommended-documents"></a>**建议的文档**
* [从客户体验总结的重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [常见问题解答 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset)
* [常见问题解答 - 密码重置注册](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset-registration)
* [常见问题解答 - 密码更改](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-change)
* [故障排除 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [故障排除 - 密码重置注册](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-registration-portal)
* [如何更新自己的密码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-update-your-own-password)
* [密码管理入门](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [最佳做法 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)


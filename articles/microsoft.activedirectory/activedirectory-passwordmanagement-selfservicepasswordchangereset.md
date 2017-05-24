<properties
    pageTitle="I'm having a problem with self-service password reset"
    description="密码管理/自助式密码更改/重置"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia, gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045826"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />


# <a name="im-having-a-problem-with-self-service-password-reset"></a>我在使用自助密码重置时遇到问题

## <a name="recommended-steps"></a>**建议的步骤**

**在组织中部署密码重置时遇到问题**

* 请务必了解许可要求：
  * 你在组织中必须至少分配有一个许可证
    * **仅限云用户** - 任何 Office 365 (O365) 付费 SKU 或 Azure AD Basic
    * **云和/或本地用户** - Azure AD Premium P1 或 P2、企业移动性 + 安全性 (EMS) 或 Secure Productive Enterprise (SPE)
    * 若要详细了解许可要求，请参阅 [Azure AD 自助密码重置的许可要求](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing)一文
* [快速入门：Azure AD 自助密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)

**我不希望用户为密码重置注册其他安全信息**

* 可以使用 API、Powershell 或 Azure AD Connect 为用户预先填充数据（电子邮件和电话属性）。 若要了解操作方法，请参阅：
  * [在无需用户注册的情况下部署密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data#set-and-read-authentication-data-using-powershell)
  * [密码重置使用哪些数据](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data)

**我希望用户为密码重置注册其他安全信息**

1. 将用户定向到 [aka.ms/ssprsetup](https://account.activedirectory.windowsazure.com/passwordreset/Register.aspx)，让他们为自助密码重置注册安全信息。

2. 为用户填充数据后（由用户自己填充或者由管理员填充），请将他们定向到 [aka.ms/sspr](https://passwordreset.microsoftonline.com/)，使他们能够重置自己的密码。

3. 如果用户仍然遇到问题，很有可能用户是**联合**用户或**密码哈希同步**用户。 这意味着密码写回服务可能存在问题。
* 有关密码写回配置的详细信息，请参阅：
  * [如何让用户重置其 Azure AD 密码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
  * [如何让用户重置或更改其本地 Active Directory 密码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-or-change-their-ad-passwords)


## <a name="recommended-documents"></a>**建议的文档**

* [常见问题解答 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset)
* [常见问题解答 - 密码重置注册](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset-registration)
* [常见问题解答 - 密码更改](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-change)
* [故障排除 - 密码重置](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [故障排除 - 密码重置注册](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-registration-portal)
* [如何更新自己的密码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-update-your-own-password)
* [密码管理入门](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [最佳做法 - 密码管理](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)


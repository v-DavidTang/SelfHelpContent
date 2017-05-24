<properties
    pageTitle="Problems with licensing"
    description="从客户体验总结的重要提示 - 提示 1"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="100"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public"
/>


# <a name="problems-with-licensing"></a>许可出现问题

## <a name="recommended-steps"></a>**建议的步骤**
**我不了解许可要求**
* 请确保已获得 Azure AD 密码重置的[有效许可证](https://azure.microsoft.com/pricing/details/active-directory/)。

* Azure AD 密码重置在 3 个层中提供：
  * Azure AD Free - 云管理员可以重置其自己的密码
  * Azure AD Basic 或任何付费 O365 订阅 - 云用户和云管理员可以重置其自己的密码
  * Azure AD Premium - 任何用户或管理员（云、联合、密码哈希同步的用户）都可以重置密码。 必须启用密码写回才能支持某些方案。


*  高级功能还包含在以下服务中：
    * 企业移动性 + 安全性 E3
    * 企业移动性 + 安全性 E5
    * Secure Productive Enterprise E3
    * Secure Productive Enterprise E5



## <a name="recommended-documents"></a>**建议的文档**
* [许可出现问题](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-1-licensing---make-sure-you-understand-the-licensing-requirements)
* [常规密码重置许可信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-customize#what-customization-options-are-available)
* [按功能密码重置许可信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords#pricing-and-availability)
* [密码写回支持的方案](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#scenarios-supported-for-password-writeback)
* [从客户体验总结的重要提示](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)


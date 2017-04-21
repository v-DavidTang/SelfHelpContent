<properties
    pageTitle="User and Group Management/Adding Users (B2B)"
    description="Azure Active Directory 自助案例提交"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="sasubram"
    displayOrder="2072"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview,userandgroups_user,userandgroups_group"
    productPesIds=""
    cloudEnvironments="public"
    />


# <a name="i-have-invited-guest-users-who-cant-redeem-their-invitations"></a>我邀请的来宾用户无法兑换其邀请
 
## <a name="recommended-steps"></a>**建议的步骤**
1. 首先，确定他们是否收到了邀请电子邮件。 尽管这种情况不太常见，但有时邀请电子邮件会被阻止在收件人的垃圾邮件文件夹中。
如果他们告知未收到电子邮件，你可以转到目录中的用户个人资料，然后尝试重发邀请。
2. 如果用户收到了邀请但无法接受邀请，原因可能是其组织已在租户中，但收件人的帐户不在租户中。 另外，其组织可能已禁用帐户的适时创建功能，而需要启用此功能才能兑换成功。 

  如果是这种情况，发生问题的原因是来宾用户的组织策略阻止了此功能。 请使用链接 https://docs.microsoft.com/powershell/msonline/v1/set-msolcompanysettings 让来宾用户联系其组织的管理员，并设置 `-AllowEmailVerifiedUsers to true`。
  
  解决此问题的另一种方法是允许从来宾用户的本地 Active Directory 同步其对象。


## <a name="recommended-documents"></a>**建议的文档**
* [将 B2B 协作来宾添加到 Azure AD 租户](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-admin-add-users)
* [B2B 协作许可](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-licensing)
* [对 B2B 协作进行故障排除](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-troubleshooting)
* [B2B 协作常见问题 (FAQ)](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-faq)
* [适用于 B2B 协作用户的多重身份验证](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-mfa-instructions)



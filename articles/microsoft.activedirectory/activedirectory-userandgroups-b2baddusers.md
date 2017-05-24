<properties
    pageTitle="User and Group Management/Adding Users (B2B)"
    description="Azure Active Directory 自助案例提交"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="sasubram"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565671"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />


# <a name="adding-b2b-collaboration-guest-users"></a>添加 B2B 协作来宾用户

## <a name="recommended-steps"></a>**建议的步骤**

### <a name="how-to-add-guest-users"></a>如何添加来宾用户
请使用“所有用户”边栏选项卡上的“新建来宾用户”按钮添加来宾用户。 输入其电子邮件地址和可选的消息，然后选择“邀请”。
 
也可以在适用于组的“添加成员”体验中使用“邀请”选项，直接将新的来宾用户添加到组中。 可以在不使用“邀请”选项的情况下，通过“添加成员”体验将现有的来宾用户添加到组中。
 
也可以在适用于组的“用户和组”@gt>“添加用户”@gt>“用户和组”体验使用“邀请”选项，直接将新的来宾用户添加到应用程序中。 可以在不使用“邀请”选项的情况下，通过“用户和组”@gt>“添加用户”@gt>“用户和组”体验将现有的来宾用户添加到组中。
 
### <a name="unable-to-invite-user-as-guest"></a>无法邀请来宾用户
请使用“所有用户”中的“新建来宾用户”按钮添加来宾用户。 只需输入其电子邮件地址和可选的消息，然后选择“邀请”即可。
 
也可以在适用于组的“添加成员”体验中使用“邀请”选项，直接将新的来宾用户添加到组中。 可以在不使用“邀请”选项的情况下，通过“添加成员”体验将现有的来宾用户添加到组中。
 
也可以在适用于组的“用户和组”@gt>“添加用户”@gt>“用户和组”体验使用“邀请”选项，直接将新的来宾用户添加到应用程序中。 可以在不使用“邀请”选项的情况下，通过“用户和组”@gt>“添加用户”@gt>“用户和组”体验将现有的来宾用户添加到组中。
 
如果仍然无法邀请，请创建支持票证并告诉我们相关问题的详细信息，我们将很乐意提供帮助。
 
### <a name="unable-to-add-an-invited-guest-user-to-the-directory"></a>无法将已邀请的来宾用户添加到目录
请使用“所有用户”中的“新建来宾用户”按钮添加来宾用户。 只需输入其电子邮件地址和可选的消息，然后选择“邀请”即可
 
也可以在适用于组的“添加成员”体验中使用“邀请”选项，直接将新的来宾用户添加到组中。 可以在不使用“邀请”选项的情况下，通过“添加成员”体验将现有的来宾用户添加到组中。
 
也可以在适用于组的“用户和组”@gt>“添加用户”@gt>“用户和组”体验使用“邀请”选项，直接将新的来宾用户添加到应用程序中。 可以在不使用“邀请”选项的情况下，通过“用户和组”@gt>“添加用户”@gt>“用户和组”体验将现有的来宾用户添加到组中。
 
如果仍然无法邀请，请创建支持票证并告诉我们相关问题的详细信息，我们将很乐意提供帮助。
 
### <a name="how-to-leave-guest-directory"></a>如何退出来宾目录
目前，退出来宾目录的唯一方法就是与另一组织的管理员联系，或者对 Microsoft 创建支持票证。
 
### <a name="unable-to-resend-invite-to-user"></a>无法向用户重新发送邀请
如果来宾用户尚未接受其邀请，请导航到该用户的个人资料，然后使用“重新发送邀请”按钮。 如果用户已接受邀请，则此处不会显示此按钮 - 在这种情况下，只需通过电子邮件将你希望他们访问的应用或资源的链接发送给他们。
 
### <a name="how-to-add-guest-users-without-invitation"></a>如何在不邀请的情况下添加来宾用户
如果邀请方组织中发出邀请的用户同时也是受邀组织（B2B 用户组织）的成员，则该 B2B 用户无需兑换该邀请。 为此，我们建议在受邀组织中邀请一个用户加入邀请方组织（你的组织）。 在资源组织中将此用户添加到来宾邀请者角色。 该用户可以使用登录 UI、PowerShell 脚本或 API 邀请受邀组织中的其他用户。 这样，该组织中的 B2B 用户便不需要兑换其邀请。
 
### <a name="invite-does-not-include-personal-messages"></a>邀请中不包含个人消息
为了遵守隐私法规，如果邀请者在资源组织（也称为邀请租户）中不具有电子邮件地址，或当应用服务主体发送邀请时，API 不会在电子邮件邀请中包含自定义消息。 如果这对你而言是一个重要方案，那么可以禁止 API 发送邀请电子邮件，并通过所选的电子邮件机制发送邮件。 请记得咨询所属组织的法律顾问，以确保通过这种方式发送的任何电子邮件均符合隐私法。
 
### <a name="unable-to-add-guest-user---getting-domain-is-not-a-verified-domain-name-in-this-directory"></a>无法添加来宾用户 - <DOMAIN> 不是此目录中的已验证域名
请使用“所有用户”中的“新建来宾用户”按钮添加来宾用户。 只需输入其电子邮件地址和可选的消息，然后选择“邀请”即可。

## <a name="recommended-documents"></a>**建议的文档**
* [将 B2B 协作来宾添加到 Azure AD 租户](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-admin-add-users)
* [B2B 协作许可](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-licensing)
* [对 B2B 协作进行故障排除](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-troubleshooting)
* [B2B 协作常见问题 (FAQ)](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-faq)
* [适用于 B2B 协作用户的多重身份验证](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-mfa-instructions)



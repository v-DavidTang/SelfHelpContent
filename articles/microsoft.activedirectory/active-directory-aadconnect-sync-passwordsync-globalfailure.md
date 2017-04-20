<properties
    pageTitle="Password synchronization does not work – No passwords are synchronized"
    description="密码同步无法正常工作 - 未同步任何密码"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="1221"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="password-synchronization-does-not-work--no-passwords-are-synchronized"></a>密码同步无法正常工作 - 未同步任何密码

## <a name="recommended-steps"></a>**建议的步骤**
* 常见的根本原因包括：

  * 未向 Azure AD Connect 与本地 Active Directory 通信时所用的 Active Directory 帐户授予“复制目录更改”和“复制所有目录更改”权限，而密码同步需要这些权限。

  * 管理员在 Azure AD Connect 向导中将用户登录方法从“密码同步”更改为其他选项（例如“与 AD FS 联合”）之后已禁用密码同步。

  * 本地 Active Directory 存在连接问题。 例如，Azure AD Connect 无法访问某些域控制器，或者防火墙阻止了[所需的端口](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-ports#table-1---azure-ad-connect-and-on-premises-ad)。

  * Azure AD Connect 服务器当前处于暂存模式。

* 若要解决该问题，请遵循[使用 Azure AD Connect 同步排查密码同步问题 - 未同步任何密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization#no-passwords-are-synchronized)部分中所述的步骤。


## <a name="recommended-documents"></a>**建议的文档**
* [使用 Azure AD Connect 同步实现密码同步](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization)  
* [使用 Azure AD Connect 同步排查密码同步问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization)  


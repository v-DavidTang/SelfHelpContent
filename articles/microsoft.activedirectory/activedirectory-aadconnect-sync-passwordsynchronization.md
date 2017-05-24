<properties
    pageTitle="Synchronizing AD to Azure AD/Password synchronization"
    description="将 AD 同步到 Azure AD/密码同步"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32142240"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="synchronizing-ad-to-azure-adpassword-synchronization"></a>将 AD 同步到 Azure AD/密码同步

## <a name="recommended-steps"></a>建议的步骤

**密码同步无法正常工作 – 未同步任何密码**

常见的根本原因包括：

  * 未向 Azure AD Connect 与本地 Active Directory 通信时所用的 Active Directory 帐户授予“复制目录更改”和“复制所有目录更改”权限，而密码同步需要这些权限。

  * 管理员在 Azure AD Connect 向导中将用户登录方法从“密码同步”更改为其他选项（例如“与 AD FS 联合”）之后已禁用密码同步。

  * 本地 Active Directory 存在连接问题。 例如，Azure AD Connect 无法访问某些域控制器，或者防火墙阻止了[所需的端口](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-ports#table-1---azure-ad-connect-and-on-premises-ad)。

  * Azure AD Connect 服务器当前处于暂存模式。

若要解决该问题，请遵循[使用 Azure AD Connect 同步排查密码同步问题 - 未同步任何密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization#no-passwords-are-synchronized)部分中所述的步骤。


**特定的用户无法使用密码同步**

常见的根本原因包括：

  * 为本地 Active Directory 用户对象启用了“用户下次登录时必须更改密码”选项。 如果启用此选项，将为该用户分配一个临时密码。该用户下次登录时，系统会提示其更改密码。 Azure AD Connect 不会将临时密码同步到 Azure AD。 若要解决此问题，请执行以下操作之一：

    * 要求该用户登录到本地应用程序（例如 Windows 桌面）并更改密码。 新密码将同步到 Azure AD；或者

    * 让管理员更新该用户的密码且不启用选项“用户下次登录时必须更改密码”选项，并与该用户共享新密码。

  * 未针对对象同步或密码同步正确配置本地 Active Directory 用户对象。

若要解决该问题，请遵循[使用 Azure AD Connect 同步排查密码同步问题 - 一个对象不同步密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization#one-object-is-not-synchronizing-passwords)文章部分中所述的步骤。


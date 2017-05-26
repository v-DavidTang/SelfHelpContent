<properties
    pageTitle="Synchronizing AD to Azure AD/Synchronization not working"
    description="将 AD 同步到 Azure AD/同步不起作用"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565591"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="synchronizing-ad-to-azure-adsynchronization-not-working"></a>将 AD 同步到 Azure AD/同步不起作用

## <a name="recommended-steps"></a>建议的步骤

**无法启动 Azure AD Connect 同步服务**

无法在 Windows 服务控制管理器中启动同步服务。 常见的根本原因包括：

* 由同步服务用作安全上下文的 Azure AD Connect 同步服务帐户的密码最近已更改。 若要解决此问题，请参阅[更改 Azure AD Connect 同步服务帐户密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)一文。

* 未向 Azure AD Connect 同步服务帐户授予“作为服务登录”权限。 有关如何授予此权限的说明，请参阅[向帐户添加“作为服务登录”权限](https://technet.microsoft.com/library/cc794944(v=ws.10).aspx)一文。

* Azure AD Connect 服务器正在将 **LocalDB** 用作数据库，该数据库具有 10-GB 的空间限制。 如果使用 LocalDB，则达到此限制后，同步服务不再能正常启动或同步。 若要从此问题恢复，请遵循[Azure AD Connect：如何从 LocalDB 10-GB 限制恢复](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)一文中所述的步骤。


**同步服务已启动但没有任何同步活动**

Azure AD Connect 同步服务似乎正在 Windows 服务控制管理器中运行，但未出现任何同步活动。 常见的根本原因包括：

* Azure Connect 向导当前已在 Azure AD Connect 服务器上打开。 如果你启动安装向导，计划程序将会暂停，直到关闭该向导。 有关此行为的详细信息，请参阅 [Azure AD Connect 同步：计划程序 - 计划程序和安装向导](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler#scheduler-and-installation-wizard)文章部分。

* Azure AD Connect 同步计划程序当前已禁用。 若要验证状态并启动同步计划程序，请参阅 [Azure AD Connect 同步：计划程序](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler)一文中的步骤。

* Azure AD Connect 服务器当前处于暂存模式。 执行导入和同步时，处于暂存模式的 Connect 服务器将会激活。 但是，它不会运行任何导出。 有关暂存模式的详细信息，请参阅 [Azure AD Connect 同步：操作任务和注意事项 - 暂存模式](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations#staging-mode)文章部分。


**同步服务无法从本地 AD 导入/导出更改**

常见的根本原因包括：

* 同步服务与本地 AD 通信时所用的 AD DS 服务帐户已被删除、其密码已更改或者其 userPrincipalName 已更改。 若要解决此问题，请参阅[更改 AD DS 帐户密码](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-addsacct-pass)一文。

* AD DS 帐户没有必要的权限，无法从本地 AD 同步更改。 若要查看权限要求，请参阅 [Azure AD Connect：帐户和权限](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-accounts-permissions)一文。

* Azure AD Connect 服务器与本地 AD 之间存在网络连接问题。 若要排查连接问题，请参阅[使用 Azure AD Connect 排查连接问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity)一文。


**同步服务无法从 Azure AD 导入/导出更改**

常见的根本原因包括：

* 同步服务与 Azure AD 通信时所用的 Azure AD 服务帐户已被删除、其密码已更改或者其 userPrincipalName 已更改。 若要解决此问题，请参阅 [Azure AD Connect 同步：如何管理 Azure AD 服务帐户](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)一文。

* Azure AD Connect 服务器与 Azure AD 之间存在网络连接问题。 若要排查连接问题，请参阅[使用 Azure AD Connect 排查连接问题](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity)一文。


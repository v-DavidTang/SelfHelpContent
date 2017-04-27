<properties
    pageTitle="Synchronization Service is started but there is no synchronization activity"
    description="同步服务已启动但没有任何同步活动"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="224"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="synchronization-service-is-started-but-there-is-no-synchronization-activity"></a>同步服务已启动但没有任何同步活动

## <a name="recommended-steps"></a>**建议的步骤**
Azure AD Connect 同步服务似乎正在 Windows 服务控制管理器中运行，但未出现任何同步活动。 常见的根本原因包括：

* Azure Connect 向导当前已在 Azure AD Connect 服务器上打开。 如果你启动安装向导，计划程序将会暂停，直到关闭该向导。 有关此行为的详细信息，请参阅 [Azure AD Connect 同步：计划程序 - 计划程序和安装向导](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler#scheduler-and-installation-wizard)文章部分。

* Azure AD Connect 同步计划程序当前已禁用。 若要验证状态并启动同步计划程序，请参阅 [Azure AD Connect 同步：计划程序](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler)一文中的步骤。

* Azure AD Connect 服务器当前处于暂存模式。 执行导入和同步时，处于暂存模式的 Connect 服务器将会激活。 但是，它不会运行任何导出。 有关暂存模式的详细信息，请参阅 [Azure AD Connect 同步：操作任务和注意事项 - 暂存模式](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations#staging-mode)文章部分。

## <a name="recommended-documents"></a>**建议的文档**
* [Azure AD Connect 同步：计划程序](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler)  
* [Azure AD Connect 同步：操作任务和注意事项](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations)  


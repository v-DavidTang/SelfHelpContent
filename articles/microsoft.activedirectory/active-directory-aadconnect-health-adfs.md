<properties
    pageTitle="Azure AD Connect Health"
    description="适用于 AD FS 的 Azure AD Connect Health 自助服务"
    service="microsoft.aad"
    resource="Microsoft_Azure_ADHybridHealth"
    authors="arluca"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32574685"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="connect-health-for-ad-fs"></a>适用于 AD FS 的 Connect Health

## <a name="troubleshooting-registration-failures"></a>排查注册失败问题
1.  请确保有权执行该操作。 默认情况下，全局管理员具有访问权限。 此外，可以使用[基于角色的访问控制](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#manage-access-with-role-based-access-control)将注册权限委派给参与者。
2.  确保所需的终结点已启用，而未被防火墙阻止。 有关详细信息，请参阅[要求](http://aka.ms/prereqs)部分。 
3.  注册可能因为出站通信受到网络层执行的 SSL 检查影响而失败。 

## <a name="troubleshooting-health-service-data-not-up-to-date"></a>排查“运行状况服务数据并非最新”问题。
1.  确保所需的终结点已启用，而未被防火墙阻止。 有关详细信息，请参阅[要求](http://aka.ms/prereqs)部分。 
2.  数据上传可能因为出站通信受到网络层执行的 SSL 检查影响而失败。 
3.  可以使用[内置的代理连接工具](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-agent-install#test-connectivity-to-azure-ad-connect-health-service)。
4.  确保已正确配置[代理设置](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-agent-install##configure-azure-ad-connect-health-agents-to-use-http-proxy)（如果适用）。

## <a name="troubleshooting-duplicate-servers-in-the-portal"></a>排查“门户中存在重复的服务器”问题。 
1.  从服务器中删除代理后，不会自动从门户中删除该服务器。 当某个具有相同名称/详细信息的服务器注册另一个代理时，将出现重复的服务器。
2.  若要从门户中删除服务器，请参阅[删除服务器或服务实例](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#delete-a-server-or-service-instance)。

## <a name="recommended-documents"></a>**建议的文档**
* [常见安装问题](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-faq#installation-questions)
* [为警报启用通知](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#enable-email-notifications)


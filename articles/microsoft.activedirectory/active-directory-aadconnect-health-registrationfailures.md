<properties
    pageTitle="Agent Registration Failures"
    description="Azure AD Connect Health 自助服务"
    service="microsoft.aad"
    resource="Microsoft_Azure_ADHybridHealth"
    authors="arluca"
    displayOrder="100"
    selfHelpType="resource"
    cloudEnvironments="public"
/>

# <a name="agent-registration-failures"></a>代理注册失败

## <a name="recommended-steps"></a>**建议的步骤**
1.    请确保你有权执行该操作。 默认情况下，全局管理员具有访问权限。 此外，可以使用[基于角色的访问控制](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#manage-access-with-role-based-access-control)将注册权限委派给参与者。
2.    确保所需的终结点已启用，而未被防火墙阻止。 有关详细信息，请参阅[要求](http://aka.ms/aadchprereqs)部分。 
3.    注册可能因为出站通信受到网络层执行的 SSL 检查影响而失败。 

## <a name="recommended-documents"></a>**建议的文档**
* [常见安装问题](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-faq#installation-questions)


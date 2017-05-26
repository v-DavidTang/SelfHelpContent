<properties
    pageTitle="Troubleshoot Health service data not up to date"
    description="Azure AD Connect Health 自助服务"
    service="microsoft.aad"
    resource="Microsoft_Azure_ADHybridHealth"
    authors="arluca"
    displayOrder="200"
    selfHelpType="resource"
    cloudEnvironments="public"
/>

# <a name="troubleshoot-health-service-data-not-up-to-date"></a>排查“运行状况服务数据不是最新的”问题

## <a name="recommended-steps"></a>**建议的步骤**
1.    确保所需的终结点已启用，而未被防火墙阻止。 有关详细信息，请参阅[要求](http://aka.ms/aadchprereqs)部分。 
2.    数据上载可能因为出站通信受到网络层执行的 SSL 检查影响而失败。 
3.    可以使用[内置的代理连接工具](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-agent-install#test-connectivity-to-azure-ad-connect-health-service)。
4.    确保已正确配置[代理设置](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-agent-install##configure-azure-ad-connect-health-agents-to-use-http-proxy)（如果适用）。

## <a name="recommended-documents"></a>**建议的文档**
* [常见安装问题](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-faq#installation-questions)


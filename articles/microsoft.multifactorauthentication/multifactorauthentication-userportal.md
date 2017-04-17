<properties
    pageTitle="MFA Server (On-premises)/User portal"
    description="MFA 服务器（本地）/用户门户"
    service="microsoft.multifactorauthentication"
    resource="Microsoft_AAD_IAM"
    authors="yossib"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32336324"
    resourceTags=""
    productPesIds="14947"
    cloudEnvironments="public"
/>


# <a name="user-portal-and-mobile-app-web-service"></a>用户门户和移动应用 Web 服务

## <a name="recommended-steps"></a>**建议的步骤**

排查用户门户问题时，可通过浏览到 Web 服务 SDK（例如 https://hostname/MultiFactorAuthWebServiceSdk/PfWsSdk.asmx）测试该门户。 如果加载了页面，则表示一切正常。 否则，可能出现了以下配置问题之一。

排查移动应用 Web 服务问题时，可通过浏览到 PfPaWs URL（例如 https://hostname/pa/PfPaWs.asmx）测试该服务。 单击“TestPfWsSdkConnection”链接，然后单击“调用”。 如果收到成功消息，则表示一切正常。 否则，可能出现了以下配置问题之一：

1. 用户名或密码不正确。
2. PfPaWs web.config 文件中的 PfWsSdk URL 不正确或不可访问。
3. PfPaWs web.config 文件中的 PfWsSdk URL 主机名不正确或不可访问。
4. 与 PfWsSdk 连接成功，但该 PfWsSdk 无法连接到 MultiFactorAuth 服务。

## <a name="recommended-documents"></a>**建议的文档**

[为 Azure 多重身份验证服务器部署用户门户](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-portal)  
[使用 Azure 多重身份验证服务器启用移动应用身份验证](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-webservice)  


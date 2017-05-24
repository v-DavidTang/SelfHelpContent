<properties
    pageTitle="MFA Server (On-Premises)/Installing or configuring RADIUS authentication"
    description="MFA 服务器（本地）/安装或配置 RADIUS 身份验证"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="kgremban"
    displayOrder="250"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="mfa_overview"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="radius-authentication"></a>RADIUS 身份验证

## <a name="recommended-steps"></a>**建议的步骤**

1. 确保 VPN/应用程序/设备中配置的 RADIUS 超时足够长，以便能够完成 MFA 身份验证。 通常，我们建议指定 60 秒。
2. 确保在 RADIUS 设备中输入的**共享机密**，与添加 RADIUS 客户端时在 MFA 服务器中输入的**共享机密**匹配。 
3. 确保添加 RADIUS 客户端时在 MFA 服务器中输入的 **IP 地址**是请求的来源 IP。 如果要保护的设备上有多个 NIC/地址，此步骤尤其重要。 使用数据包捕获应该可以确定这一点。 使用捕获还可以帮助你确认通信是否通过防火墙进行。 

## <a name="recommended-documents"></a>**建议的文档**

- [将 RADIUS 身份验证与 Azure 多重身份验证服务器集成](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-radius)  
- [使用 RADIUS 的远程桌面网关和 Azure 多重身份验证服务器](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-rdg)  
- [使用 Azure 多重身份验证和第三方 VPN 解决方案的高级方案](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-advanced-vpn-configurations)  
- [将现有 NPS 基础结构与 Azure 多重身份验证集成](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-nps-extension)  


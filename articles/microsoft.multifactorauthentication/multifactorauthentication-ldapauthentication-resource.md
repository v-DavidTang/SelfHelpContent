<properties  
    pageTitle="MFA Server (On-Premises)/LDAP authentication" 
    description="LDAP 身份验证" 
    service="microsoft.aad" 
    resource="Microsoft_AAD_IAM" 
    authors="kgremban" 
    displayOrder="240"
    selfHelpType="resource" 
    supportTopicIds="" 
    resourceTags="mfa_overview"
    productPesIds="" 
    cloudEnvironments="public" 
 /> 

# <a name="ldap-authentication"></a>LDAP 身份验证 

## <a name="recommended-steps"></a>**建议的步骤** 

请确保添加 LDAP 客户端时在 MFA 服务器中输入的 IP 地址是请求的来源 IP，尤其是要保护的设备上有多个 NIC/地址时。  使用数据包捕获应该可以查看此信息。 使用捕获还可以帮助确认通信是否通过防火墙进行。 

在“目录集成”部分中，确保已正确配置目标 LDAP 服务器：
   
- 该服务器可以是主机名或 IP。 如果想要指定多个服务器，可以指定一个备份并以分号分隔。 
- 基 DN 应是要在目录中查询的位置。 例如 dc=domain,dc=com。 
- 如果使用 SSL，请使用简单的或 Windows 优先的 SSL 测试，确保正常通信。  如果能够正常通信，则可能是所用的证书存在问题。 请确保证书安装在本地并且受 LDAP 目录的信任。 
- 为每台计算机设置绑定用户名和密码，因为这些凭据将存储在本地 Windows 存储中。  如果有多个 MFA 服务器，需在想要处理 LDAP 身份验证的每台服务器中输入此信息 
- 使用测试按钮来确保正常通信。  这可以确保能够绑定。  也可以转到“用户”部分，并选择要对其测试 LDAP 身份验证的特定用户。 

## <a name="recommended-documents"></a>**建议的文档** 

- [LDAP 身份验证和 Azure 多重身份验证](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-ldap)  
- [Azure MFA 服务器与 AD/LDAP 之间的目录集成](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-dirint)  
- [Azure MFA 服务器概述视频](https://azure.microsoft.com/resources/videos/multi-factor-authentication-server)  

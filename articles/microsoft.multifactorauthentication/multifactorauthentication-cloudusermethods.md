<properties
  pageTitle="Cloud-based MFA/User MFA methods issues (cloud)"
  description="用户 MFA 方法问题"
  service="microsoft.multifactorauthentication"
  resource=""
  authors="kgremban"
  selfHelpType="generic"
  supportTopicIds="32570992"
  productPesIds="14947"
  cloudEnvironments="public"
/>


# <a name="user-mfa-methods-issues"></a>用户 MFA 方法问题

## <a name="recommended-steps"></a>**建议的步骤**

### <a name="text-messages-never-arrive-or-are-significantly-delayed"></a>短信一直收不到或者有很长时间的延迟 

短信问题的原因通常与电话接收信号强度、本地 PBX 和电话网络的语音拨号处理方式、线路干扰、通话本底噪声、单个设备的技术故障以及 MFA 服务器外部的类似原因有关。 如果用户经常无法可靠地接收短信，请告诉他们改用移动应用验证方法。

### <a name="what-can-i-do-to-ensure-users-who-dont-have-access-to-their-phones-are-able-to-sign-in"></a>如何确保无法使用电话的用户能够登录？ 

请确保用户已配置多种验证方法，例如办公电话。 请告诉他们再次尝试登录，但需要在登录页上选择另一种验证方法。

## <a name="recommended-documents"></a>**建议的文档**

[管理云中 Azure 多重身份验证的用户设置](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-manage-users-and-devices)  
[管理和支持用户帐户](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-faq#manage-and-support-user-accounts) 

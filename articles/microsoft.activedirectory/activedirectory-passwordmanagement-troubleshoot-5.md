<properties
    pageTitle="Tip 6: WRITEBACK - Ensure you enable the correct permissions, firewall rules, and connection settings for password writeback"
    description="从客户体验总结的重要提示 - 提示 6"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="600"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public"
 />

# <a name="tip-6-writeback---configuration"></a>提示 6：写回 - 配置
## <a name="ensure-you-enable-the-correct-permissions-firewall-rules-and-connection-settings-for-password-writeback"></a>确保为密码写回启用正确的权限、防火墙规则和连接设置
为了使写回正常工作，必须确保：

1. 已为使用密码写回功能的用户设置适当的 **Active Directory 权限**，使之有权在 AD 中修改其密码和帐户解锁标志
2. 已打开适当的**防火墙端口**，因此密码写回服务可以通过出站连接安全地与外界通信
3. 已为密码重置服务 URL（例如服务总线）设置适当的**防火墙例外**
4. **代理和防火墙不终止空闲的出站连接**。建议将空闲时间设置为至少 10 分钟

针对密码写回配置权限和防火墙规则时，如需完整的故障排除指南列表和具体的指导原则，请转到[此处](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)：






[在 DOCS.com 上查看](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-6-writeback---ensure-you-enable-the-correct-permissions-firewall-rules-and-connection-settings-for-password-writeback)

## <a name="recommended-documents"></a>**建议的文档**
* [故障排除 - 密码写回](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [密码写回事件日志错误代码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [故障排除 - 密码写回连接](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [写回部署 - 步骤 3：配置防火墙](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#step-3-configure-your-firewall)
* [写回部署 - 步骤 4：设置适当的权限](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#step-4-set-up-the-appropriate-active-directory-permissions)
* [常见问题解答 - 密码写回](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)


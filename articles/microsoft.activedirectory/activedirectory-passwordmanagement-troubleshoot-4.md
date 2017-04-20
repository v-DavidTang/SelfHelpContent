<properties
    pageTitle="Tip 5: WRITEBACK - Look at the application event log on your AAD Connect machine to troubleshoot password writeback"
    description="从客户体验总结的重要提示 - 提示 5"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="500"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public"
 />

# <a name="tip-5-writeback---aad-connect-application-event-log"></a>提示 5：写回 - AAD Connect 应用程序事件日志
## <a name="look-at-the-application-event-log-on-your-aad-connect-machine-to-troubleshoot-password-writeback"></a>查看 AAD Connect 计算机上的应用程序事件日志，排查密码写回问题
Azure AD Connect 应用程序事件日志包含大量的日志记录信息，这些信息实时描述与密码写回服务相关的大多数事件。 若要访问该日志，请执行以下步骤：

1. 登录到 **Azure AD Connect** 计算机
2. 按“开始”并键入“事件查看器”，打开“Windows 事件查看器”
3. 打开“应用程序”事件日志
4. 查找来自 **PasswordResetService** 或 **ADSync** 的事件，详细了解可能出现的问题

有关可能出现在此日志中的事件的完整列表以及更多有关密码写回的故障排除指南，请参阅**建议的文档**：




[在 DOCS.com 上查看](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-5-writeback---look-at-the-application-event-log-on-your-aad-connect-machine-to-troubleshoot-password-writeback)

## <a name="recommended-documents"></a>**建议的文档**
* [故障排除 - 密码写回](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback)
* [密码写回事件日志错误代码](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#password-writeback-event-log-error-codes)
* [故障排除 - 密码写回连接](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback-connectivity)
* [写回部署 - 步骤 3：配置防火墙](#step-3-configure-your-firewall)
* [写回部署 - 步骤 4：设置适当的权限](#step-4-set-up-the-appropriate-active-directory-permissions)
* [常见问题解答 - 密码写回](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-writeback)
* [你需要帮助时应包含的信息](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)


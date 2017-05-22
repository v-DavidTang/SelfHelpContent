<properties
    pageTitle="Problems configuring policy for an application"
    description="为应用程序配置策略时遇到问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="problems-configuring-policy-for-an-application"></a>为应用程序配置策略时遇到问题

**不知道哪些应用程序支持条件访问**

并非所有应用程序都支持条件访问。 支持条件访问需要使用新式身份验证以及允许验证设备标识的集成。 我们会不断增加支持的应用程序数目。 在以下文档中可以找到最新的应用程序列表。
<br>
[哪些云应用程序支持条件访问](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-technical-reference)<br>
[哪些桌面和移动应用程序支持条件访问](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-supported-apps)

**不知道如何保护旧式桌面应用程序**

采用新式身份验证的浏览器和应用程序支持条件访问策略。 不采用新式身份验证的旧版 Office（例如 Office 2010 或 Office 2013）使用不同的安全协议，这种协议需要在 ADFS 中锁定。 编写 ADFS 颁发授权规则可以解决此问题。
<br><br>
以下文档介绍了如何使用 ADFS 锁定旧式协议：
<br>
[如何为 Office 365 SharePoint 和 Exchange 配置条件访问](http://aka.ms/csforexchange)

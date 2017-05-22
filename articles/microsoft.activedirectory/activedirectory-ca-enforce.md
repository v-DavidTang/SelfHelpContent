<properties
    pageTitle="Problems with policy not being enforced"
    description="不强制实施策略的问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="problems-with-policy-not-being-enforced"></a>不强制实施策略的问题


**根据所用的移动应用程序或桌面应用程序出现不同的结果。**

采用新式身份验证的浏览器和应用程序支持条件访问策略。 不采用新式身份验证的旧版 Office（例如 Office 2010 或 Office 2013）使用不同的安全协议，这种协议需要在 ADFS 中锁定。 编写 ADFS 颁发授权规则可以解决此问题。
<br><br>
以下文档介绍了如何使用 ADFS 锁定旧式协议：
<br>
[如何为 Office 365 SharePoint 和 Exchange 配置条件访问](http://aka.ms/csforexchange)


**未看到针对任何应用程序强制实施条件访问策略**

条件访问策略更改最长可能需要五分钟才会生效。 如果刚刚做了策略更改，请在五分钟后重试。 如果这样做无法解决问题，可以检查策略，并确保所有条件适用。 例如，该策略是否已应用到所要测试的用户和应用程序。
<br><br>
有关详细信息，请参阅：
<br>
[如何使用条件来触发策略控制](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)



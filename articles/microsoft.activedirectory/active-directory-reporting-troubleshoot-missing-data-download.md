<properties
    pageTitle="I can’t find any data in the Azure Active Directory activity logs I have downloaded"
    description="我在下载的 Azure Active Directory 活动日志中找不到任何数据"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit,azureadrreports_missingdata_signin"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-find-any-data-in-the-azure-active-directory-activity-logs-i-have-downloaded"></a>我在下载的 Azure Active Directory 活动日志中找不到任何数据

## <a name="recommended-steps"></a>**建议的步骤**

当你在 Azure 门户中下载活动日志时，我们将规模限制为 120K 条记录，最新的记录排在最前面。

- 可以在任何给定时间使用 [Azure AD 报告 API](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started) 提取多达一百万条的记录。 我们建议的方法是，按计划运行脚本，通过调用报告 API 以增量方式获取某个时段（例如每日或每周）的记录。

## <a name="recommended-documents"></a>**建议的文档**
[Azure Active Directory 报告常见问题](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)


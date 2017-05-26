<properties
    pageTitle="I can't see more than 30 days of report data "
    description="如何查看 30 天以上的报告数据？"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit,azureadrreports_missingdata_signin"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-see-more-than-30-days-of-report-data"></a>无法查看 30 天以上的报表数据

## <a name="recommended-steps"></a>**建议的步骤**

根据你持有的许可证，Azure Active Directory 操作会按以下持续时间存储活动报告：

| 报表           | Azure AD Free | Azure AD Premium P1 | Azure AD Premium P2 |
| ---              | ---           | ---                 | ---                 |
| 目录审核  |    7 天       | 30 天             | 30 天 |
| 登录活动 |    7 天       | 30 天             | 30 天 |


- 如果需要查看超过 30 天的数据，可以使用报告 API 以编程方式提取数据，然后在本地存储这些数据。 或者，可将审核日志集成到 SIEM 系统中。



## <a name="recommended-documents"></a>**建议的文档**

- [Azure Active Directory 报告保留策略](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-retention)  
- [报告 API 入门](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started)  
- [Azure Active Directory 报告常见问题](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)



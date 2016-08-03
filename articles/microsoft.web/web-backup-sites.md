<properties
    pageTitle="configuration and management/backup"
    description="配置和管理/备份"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32542208"
    resourceTags=""
    productPesIds="14748"
    cloudEnvironments="public"
/>


# 配置和管理/备份

## **建议的步骤**
执行 Web 应用备份时看到了“部分成功”消息？ 此问题的常见原因之一是某些文件已被应用程序使用，因此，当你执行备份时，这些文件被锁定。如果从备份过程中排除这些文件并选择仅备份所需的文件，则也许可以避免此错误。 有关如何从备份过程中排除文件以及如何选择仅备份所需的文件，参阅以下文章。 备份状态代码解释：

1. 0 – InProgress：备份已启动但尚未完成。
2. 1 – Failed：备份未成功。
3. 2 – Succeeded：备份成功完成。
4. 3 – TimedOut：备份未按时完成，已被取消。
5. 4 – Created：备份请求已排队，但尚未启动。
6. 5 – Skipped：由于计划触发了太多备份，备份尚未进行。
7. 6 – PartiallySucceeded：备份成功，但有些文件因无法读取而未备份。 之所以会发生这种情况，通常是因为在这些文件上放置了排他锁。
8. 7 – DeleteInProgress：已请求删除备份，但尚未删除。
9. 8 – DeleteFailed：无法删除备份。 之所以会发生这种情况，是因为用于创建备份的 SAS URL 已过期。
10. 9 – Deleted：已成功删除备份。

## **建议的文档**
[备份 Web 应用 – 要求、限制和其他信息](https://azure.microsoft.com/documentation/articles/web-sites-backup/)<br>
[如何还原 Web 应用](https://azure.microsoft.com/documentation/articles/web-sites-restore/)<br>
[使用 REST 备份和还原 App Service 应用](https://github.com/Azure/azure-content/blob/master/articles/app-service-web/websites-csm-backup.md)<br>
[如何从备份过程中排除文件以及如何选择仅备份所需的文件](http://www.zainrizvi.io/2015/06/05/creating-partial-backups-of-your-site-with-azure-web-apps/)



<!--HONumber=Jul16_HO4-->



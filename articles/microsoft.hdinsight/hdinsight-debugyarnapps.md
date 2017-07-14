<properties
    pageTitle="I'm having an issues with my YARN application"
    description="YARN 应用程序出现问题"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds="32511173"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>


# YARN 应用程序出现问题
<a id="im-having-an-issues-with-my-yarn-application" class="xliff"></a>

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>
 调试 YARN 应用程序问题时，以下各项可能会有帮助。
 
 1. **YARN Timeline Server**：YARN Timeline Server 提供有关已完成的应用程序的常规信息，以及特定于框架的应用程序信息。
 2. **YARN 应用程序日志**：调试问题时，应用程序日志可能很有作用。 聚合日志存储在 `/app-logs/<user>/logs/<applicationId>` 路径中
 3. **YARN CLI 工具**：使用 SSH 连接到 HDInsight 群集后，可以使用 `yarn logs -applicationId <applicationId> -appOwner <user-who-started-the-application>` 收集 YARN 日志
 4. **YARN ResourceManager UI**：将 /yarnui/hn/logs/ 添加到群集 URL 的末尾即可查看 YARN 日志 
 
## **建议的文档**
<a id="recommended-documents" class="xliff"></a>
[在基于 Linux 的 HDInsight 上访问 YARN 应用程序日志](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-access-yarn-app-logs-linux)<br>


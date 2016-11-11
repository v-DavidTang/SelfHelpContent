<properties
    pageTitle="Availability, performance, and application issues/problems with webjobs"
    description="可用性、性能和应用程序问题/Web 作业问题"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32542219"
    resourceTags=""
    productPesIds="14748,16170"
    cloudEnvironments="public"
/>


# 可用性、性能和应用程序问题/Web 作业问题
## **建议的步骤**

1. 要使计划的 Web 作业正常运行，需要将网站配置为始终打开。 有关详细信息，请查看下面的 Wiki 链接。 
2. 若要查看计划的 Web 作业的计划程序日志，需使用“获取触发的 Web 作业”API。为此请转到 URL：https://{站点名称}.scm.azurewebsites.net/api/triggeredwebjobs/{作业名称}（删除作业名称可查看所有已触发的 Web 作业）。
3. 可以在停止 Web 应用时运行 Web 作业。  如果 Web 作业按计划运行，则不管 Web 应用的状态如何，该作业都将继续按该计划运行，直到使用 WEBJOBS_STOPPED 将它删除或禁用。

## **建议的文档**
[Web 作业 Wiki](https://github.com/projectkudu/kudu/wiki/Web-jobs)<br>
[Web 作业资源列表](https://azure.microsoft.com/documentation/articles/websites-webjobs-resources/)



<!--HONumber=Oct16_HO3-->



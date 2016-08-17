<properties
    pageTitle="可用性、性能和应用程序问题/HTTP 5xx 错误"
    description="可用性、性能和应用程序问题/HTTP 5xx 错误"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32542218"
    resourceTags=""
    productPesIds="14748"
    cloudEnvironments="public"
/>


# 可用性、性能和应用程序问题/HTTP 5xx 错误

## **建议的步骤**
使用实时 HTTP 流量图表评估 HTTP 错误的影响

1. 识别应用程序性能不良的实例（每个实例的站点指标）
2. 尝试使用“高级应用程序重启”来解决问题
3. 识别 App Service 计划中 CPU/内存消耗最高的 Web 应用（每个实例的 App Service 计划指标）
4. 启用应用程序日志记录（文件系统）
5. 启用失败请求跟踪

## **建议的文档**
[排查应用的 HTTP 5xx 错误](https://azure.microsoft.com/documentation/articles/app-service-web-troubleshoot-http-502-http-503/)<br>
[远程分析 App Service 上运行的 .NET 应用程序](https://azure.microsoft.com/blog/remote-profiling-support-in-azure-app-service/)<br>
[如何设置自动修复](http://azure.microsoft.com/blog/2014/02/06/auto-healing-windows-azure-web-sites/)<br>
[尝试使用本地缓存来减少存储故障引起的应用重启](https://azure.microsoft.com/documentation/articles/app-service-local-cache/)<br>
[本地缓存视频](https://channel9.msdn.com/Shows/Cloud+Cover/Episode-201-Azure-Web-App-Local-Cache-with-Cory-Fowler)<br>
[HTTP 状态代码和故障排除提示](https://blogs.msdn.microsoft.com/waws/2016/06/22/troubleshooting-azure-app-service-apps-using-web-server-logs/)



<!--HONumber=Aug16_HO1-->



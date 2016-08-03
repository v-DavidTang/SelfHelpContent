<properties
    pageTitle="availability, performance, and application issues/slow performance"
    description="可用性、性能和应用程序问题/运行性能缓慢"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32457411"
    resourceTags=""
    productPesIds="14748"
    cloudEnvironments="public"
/>


# 可用性、性能和应用程序问题/运行性能缓慢

## **建议的步骤**
1. 识别应用程序性能不良的实例
2. 尝试使用“高级应用程序重启”来解决问题（每个实例的站点指标）
3. 识别 App Service 计划中 CPU/内存消耗最高的 Web 应用（每个实例的 App Service 计划指标）
4. 向上扩展 App Service 计划可以解决某些性能问题
5. 向外扩展 App Service 计划可以缓解高负载问题

## **建议的文档**
[监视、诊断和排查性能问题](https://azure.microsoft.com/documentation/articles/app-service-web-troubleshoot-performance-degradation/)<br>
[在 Node.js 中排查内存泄漏和 CPU 使用率问题](http://blogs.msdn.com/b/azureossds/archive/2015/08/23/troubleshoot-finding-memory-leaks-and-cpu-usage-in-node-js-azure-web-app.aspx)<br>
[如何设置自动修复](http://azure.microsoft.com/blog/2014/02/06/auto-healing-windows-azure-web-sites/)<br>
[排查 Web 应用的 HTTP 502 或 503 错误](https://azure.microsoft.com/documentation/articles/app-service-web-troubleshoot-http-502-http-503/)<br>
[加速 Azure Web 应用中 WordPress 站点的 10 种方法](https://azure.microsoft.com/blog/10-ways-to-speed-up-your-wordpress-site-on-azure-websites/)<br>
[WordPress 计划作业 (wp-cron.php) 和速度缓慢问题](https://blogs.msdn.microsoft.com/azureossds/2015/06/11/wordpress-scheduled-jobs-wp-cron-php-and-slowness/)<br>
[优化 Azure Linux VM 上 MySQL 数据库的性能](https://blogs.msdn.microsoft.com/azureossds/2015/03/27/performance-tuning-mysql-database-on-azure-linux-vms/)



<!--HONumber=Jul16_HO4-->



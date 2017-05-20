<properties
    pageTitle="worker role (paas)/application and service availability/role startup and recycling"
    description="辅助角色 (PAAS)/应用程序和服务可用性/角色启动和回收"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32422590"
    resourceTags=""
    productPesIds="13185"
    cloudEnvironments="public"
/>


# <a name="worker-role-paasapplication-and-service-availabilityrole-startup-and-recycling"></a>辅助角色 (PAAS)/应用程序和服务可用性/角色启动和回收

## <a name="recommended-steps"></a>**建议的步骤**

角色实例可在 **已启动** 、 **正在初始化** 、 **忙碌** 和 **已停止** 这几种状态之间循环。 这种情况可能表示应用程序代码、包或配置文件存在问题。 <br>

## <a name="recommended-steps"></a>**建议的步骤**
1. 在云服务的“概述”边栏选项卡中查看不处于“就绪”状态的角色实例的详细错误消息。 <br>

2. 检查详细错误消息是否与导致角色 **忙碌** 或 **正在回收** 的常见问题相符： <br>
  * [角色在初始化或停止时引发未经处理的异常] (https://blogs.msdn.microsoft.com/kwill/2013/08/20/troubleshooting-scenario-1-role-recycling/) <br>
  * [导致“忙碌”状态的启动任务] (https://blogs.msdn.microsoft.com/kwill/2013/09/06/troubleshooting-scenario-3-role-stuck-in-busy/) <br>
  * [启动任务在正常运行一段时间后导致“正在回收”状态](https://blogs.msdn.microsoft.com/kwill/2013/08/26/troubleshooting-scenario-2-role-recycling-after-running-fine-for-2-weeks/) <br>
  * [缺少运行时依赖项] (https://blogs.msdn.microsoft.com/kwill/2013/10/03/troubleshooting-scenario-7-role-recycling/) <br>
  * [清理/删除文件失败导致角色回收] (https://blogs.msdn.microsoft.com/kwill/2013/09/23/troubleshooting-scenario-6-role-recycling-after-running-for-some-time/) <br>
  * [角色从 Run 方法返回，但应无限期阻塞] (https://msdn.microsoft.com/library/microsoft.windowsazure.serviceruntime.roleentrypoint.run.aspx) <br>

有关如何排查此类问题的详细信息，请参阅以下链接：<br>

## <a name="recommended-documents"></a>**建议的文档**
  [导致角色回收的常见问题](https://azure.microsoft.com/documentation/articles/cloud-services-troubleshoot-common-issues-which-cause-roles-recycle/)<br>
  [排查和解决无法启动云服务角色的常用步骤](https://azure.microsoft.com/documentation/articles/cloud-services-troubleshoot-roles-that-fail-start/)<br>
  [排查云服务的常见问题 - 角色回收和启动](http://blogs.msdn.com/b/kwill/archive/2013/08/09/windows-azure-paas-compute-diagnostics-data.aspx)<br>
  [调试云服务的各种方法](https://docs.microsoft.com/azure/vs-azure-tools-debugging-cloud-services-overview)<br>
  [排查云服务部署问题](https://azure.microsoft.com/documentation/articles/cloud-services-troubleshoot-deployment-problems/)


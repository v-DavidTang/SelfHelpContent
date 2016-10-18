<properties
    pageTitle="My Role is Busy or Recycling"
    description="角色处于“忙碌”或“正在回收”状态"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="jluk"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 角色处于“忙碌”或“正在回收”状态
角色实例可在**“已启动”**、**“正在初始化”**、**“忙碌”**和**“已停止”**这几种状态之间循环。 这种情况可能表示应用程序代码、包或配置文件存在问题。 <br>

## **建议的步骤**
1. [在此处查看详细错误消息](https://manage.windowsazure.com/microsoft.com#Workspaces/CloudServicesExtension/list)，获取有关错误消息的详细信息。 <br>

2. 检查详细错误消息是否与导致角色**“忙碌”**或**“正在回收”**的常见问题相符： <br>
  * [角色在初始化或停止时引发未经处理的异常] (https://blogs.msdn.microsoft.com/kwill/2013/08/20/troubleshooting-scenario-1-role-recycling/) <br>
  * [导致“忙碌”状态的启动任务] (https://blogs.msdn.microsoft.com/kwill/2013/09/06/troubleshooting-scenario-3-role-stuck-in-busy/) <br>
  * [启动任务在正常运行一段时间后导致“正在回收”状态](https://blogs.msdn.microsoft.com/kwill/2013/08/26/troubleshooting-scenario-2-role-recycling-after-running-fine-for-2-weeks/) <br>
  * [缺少运行时依赖项] (https://blogs.msdn.microsoft.com/kwill/2013/10/03/troubleshooting-scenario-7-role-recycling/) <br>
  * [清理/删除文件失败导致角色回收] (https://blogs.msdn.microsoft.com/kwill/2013/09/23/troubleshooting-scenario-6-role-recycling-after-running-for-some-time/) <br>
  * [角色从 Run 方法返回，但应无限期阻塞] (https://msdn.microsoft.com/library/microsoft.windowsazure.serviceruntime.roleentrypoint.run.aspx) <br>

参阅以下文档，详细了解如何解决此类问题。 <br>

## **建议的文档**
[Azure PaaS 计算诊断数据](http://blogs.msdn.com/b/kwill/archive/2013/08/09/windows-azure-paas-compute-diagnostics-data.aspx) <br>
[导致角色回收的常见问题](https://azure.microsoft.com/documentation/articles/cloud-services-troubleshoot-common-issues-which-cause-roles-recycle/) <br>


<!--HONumber=Oct16_HO1-->



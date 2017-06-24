<properties
    pageTitle="CloudServices RCA"
    description="RCA - 计划内维护 - 角色回收"
    infoBubbleText="发现最近已重新启动。 请参阅右侧的详细信息。"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="chiragpa"
    displayOrder=""
    articleId="RoleRecycle_GuestOSUpdate_All_Instances_Down"
    diagnosticScenario="CloudServiceRolecyle"
    selfHelpType="rca"
    supportTopicIds="32422590"
    resourceTags=""
    productPesIds="13185"
    cloudEnvironments="public"
/>

# <a name="we-ran-diagnostics-on-your-resource-and-found-an-issue"></a>我们对你的资源运行了诊断并发现了问题

<!--issueDescription-->
## <a name="role-recycle-incident-diagnostic-information-for-rolename--rolename--"></a>**[RoleName] 的角色回收事件诊断信息<!--($RoleName)-->：** ##

从 **[StartTime]<!--($StartTime)--> (UTC)** 到 **[EndTime]<!--($EndTime)--> (UTC)**，角色 **[RoleName]<!--($RoleName)--> 的可用性已受到影响。  在此时间范围内，实例 **[ListRoleInstanceName]<!--($ListRoleInstanceName)--> 已关闭。 这一预期事件由 **Azure 启动的计划内维护操作**所致。  

<!--/issueDescription-->

此计划内维护更新需要重新启动角色实例，以便将所需的更新应用到基础结构。 角色实例在我们修补基础结构时关闭，然后角色实例已重启。<br> 若要了解有关 Azure 上计划内维护的详细信息，请参阅以下文章：<br>
* [Azure 中云服务的计划内维护](https://blogs.msdn.microsoft.com/kwill/2012/09/19/role-instance-restarts-due-to-os-upgrades/)<br>

为了确保提高 Azure 中应用程序的保护和冗余级别，我们建议为每个 Web 角色\辅助角色配置两个或更多个实例。<br>
若要详细了解可能会影响云服务可用性的计划内维护及其通知和缓解策略，请参阅以下文章：<br>
* [角色实例因计划内维护而重启](https://blogs.msdn.microsoft.com/kwill/2012/09/19/role-instance-restarts-due-to-os-upgrades/)<br>

若要详细了解以往的所有来宾 OS 版本及其相应的安全更新，请参阅以下文章：<br>
* [来宾 OS 版本](https://docs.microsoft.com/azure/cloud-services/cloud-services-guestos-update-matrix#releases)<br>
* [来宾 OS 上的安全更新](https://docs.microsoft.com/azure/cloud-services/cloud-services-guestos-msrc-releases)<br>

订阅[来宾 OS 更新 RSS 源](https://docs.microsoft.com/azure/cloud-services/cloud-services-guestos-update-matrix)，以接收有关所有来宾 OS 更改的最新通知<br>

对于这可能给你带来的任何不便，我们深表歉意。 我们将不断努力改进 Azure 平台，以提高云服务的可用性。

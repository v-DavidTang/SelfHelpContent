<properties
    pageTitle="管理我的中心/我如何实现灾难恢复"
    description="管理我的中心/我如何实现灾难恢复"
    service="microsoft.notificationhubs"
    authors="faridabharmal"
    displayOrder=""
    selfHelpType="generic"
    resource="namespaces"
    resourceTags="notificationHubs"
    productPesIds="15973"
    supportTopicIds="32565569"
    cloudEnvironments="public"
/>


# <a name="manage-my-hubhow-do-i-achieve-disaster-recovery"></a>管理我的中心/我如何实现灾难恢复

## <a name="recommended-steps"></a>**建议的步骤**
* 通知中心会自动保存元数据，因此，在灾难发生后的短暂停机之后，中心元数据将恢复，并且中心将使用相同的 url 和密钥启动并正常运行。 
* 但是，所有设备信息将会丢失。 若要恢复设备信息，请为设备数据设置频繁的导出作业，以便备份其信息。 新的中心可用时，请导入设备数据，还原中心的完整原始状态。




<!--HONumber=Jan17_HO2-->



<properties
    pageTitle="I can't delete the StorSimple Device Manager or StorSimple device from Azure portal"
    description="无法从 Azure 门户中删除 StorSimple 设备管理器或 StorSimple 设备"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="9"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="8000Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-delete-the-storsimple-device-manager-or-storsimple-device-from-azure-portal"></a>无法从 Azure 门户中删除 StorSimple 设备管理器或 StorSimple 设备。


## <a name="recommended-steps"></a>**建议的步骤**

仅当没有任何设备与 StorSimple 设备管理器服务相连接时，才可以删除此服务。 请确保没有任何已注册的设备，然后重试删除操作。

若要删除某个设备，首先需要停用该设备。

在停用设备之前，如果不想要保留与存储帐户中的设备相关联的云数据，请确保删除设备卷、备份策略和卷容器。

停用设备后，即可删除该设备。 这样，便可以避免产生任何设备和数据使用费。


## <a name="recommended-documents"></a>**建议的文档**

[删除 StorSimple 设备管理器服务](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-service#delete-a-service)<br>
[停用和删除 StorSimple 设备](https://docs.microsoft.com/azure/storsimple/storsimple-8000-deactivate-and-delete-device)

<properties
    pageTitle="How can I move data from one device to another device"
    description="如何将数据从一台设备移到另一台设备"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="8000Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="how-can-i-move-data-from-one-device-to-another-device"></a>如何将数据从一台设备移到另一台设备

将数据从一台 StorSimple 设备迁移到另一台设备时，请注意以下信息：

## <a name="recommended-steps"></a>**建议的步骤**

* 如果要将数据从 5000-7000 系列迁移到 StorSimple 8000 系列设备，请转到 [Microsoft Azure StorSimple 8000 系列迁移指南](https://gallery.technet.microsoft.com/Azure-StorSimple-50007000-c1a0460b)了解详细说明。
* 如果要从其他存储设备迁移，请转到[有关将数据迁移到 Storsimple 的指南](http://download.microsoft.com/download/9/4/A/94AB8165-CCC4-430B-801B-9FD40C8DA340/Migrating%20Data%20to%20StorSimple%20Volumes_09-02-15.pdf)
* 如果使用设备故障转移来更改数据所有权，请注意：
 * 如果已将两个设备注册到不同的 StorSimple 设备管理器，则不支持故障转移。
 * 仅当已将两个设备注册到同一个 StorSimple 设备管理器服务时，才能进行故障转移。

## <a name="recommended-documents"></a>**建议的文档**

[StorSimple 8000 系列设备的故障转移和灾难恢复](https://docs.microsoft.com/azure/storsimple/storsimple-8000-device-failover-disaster-recovery)

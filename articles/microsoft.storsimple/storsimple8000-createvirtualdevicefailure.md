<properties
    pageTitle="I can't create 8010 or 8020 cloud appliances in an Azure region"
    description="无法在 Azure 区域中创建 8010 或 8020 云设备"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="8000Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-create-8010-or-8020-cloud-appliances-in-an-azure-region"></a>无法在某个 Azure 区域中创建 8010 或 8020 云设备

如果无法在特定的区域中创建 StorSimple 云设备，原因可能是：

## <a name="recommended-steps"></a>**建议的步骤**

* Azure 虚拟机大小在该区域中不受支持。 StorSimple 云设备 8010 是标准的 A3 虚拟机，8020 是标准的 DS3 v1 虚拟机。 请参阅 [Azure VM 支持的区域](https://azure.microsoft.com/regions/services/)确定支持标准 A3 和标准 DS3 v1 的区域。
* 服务注册密钥过时，需要重新生成。 重新生成服务注册密钥，然后尝试创建云设备。 有关详细信息，请参阅[重新生成服务注册密钥](https://aka.ms/ss8000-ts-regenkey)。
* 此问题可能是预配虚拟设备时指定的虚拟网络与子网组合的相关网络连接问题造成的。 请参阅[网络连接故障排除指南](https://aka.ms/ss-sca-troubleshoot-connect)了解详细信息，然后重试操作。

## <a name="recommended-documents"></a>**建议的文档**

[在 Azure 中部署和管理 StorSimple 虚拟设备](https://docs.microsoft.com/azure/storsimple/storsimple-8000-cloud-appliance-u2)<br>
[排查 StorSimple 虚拟设备 Internet 连接错误](https://docs.microsoft.com/azure/storsimple/storsimple-8000-cloud-appliance-u2#troubleshoot-internet-connectivity-errors)


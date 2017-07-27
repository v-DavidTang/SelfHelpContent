<properties
    pageTitle="I can't register the device to the service"
    description="无法将设备注册到服务"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="8000Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-register-the-device-to-the-service"></a>无法将设备注册到服务。

如果注册失败，原因可能是下列其中一项：

## <a name="recommended-steps"></a>**建议的步骤**

* 注册密钥可能不正确。
 * 验证使用的是否是适用于物理设备系列的 StorSimple 设备管理器的注册密钥。
 * 若要获取服务注册密钥，请转到“StorSimple 设备管理器”边栏选项卡，然后转到“管理” > “密钥”。 有关详细说明，请转到[获取服务注册密钥](https://aka.ms/ss8000-ts-regenkey)。
* 设备时间可能不同步。
 * 在设备的 Windows PowerShell 界面中，运行 *Set-HcsSystem -Timezone* 命令。 调整时区。 确保采用正确的大小写输入时区。 每个首字母需大写，例如“Pacific Standard Time”。
 * 使用 *Sync-HcsTime* cmdlet 显示设备时间并强制与 NTP 服务器进行时间同步。 有关详细信息，请转到[使用 Sync-HcsTime cmdlet 进行故障排除](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#troubleshoot-with-the-sync-hcstime-cmdlet)。
* 代理服务器设置可能不正确。 注册时确保使用有效的代理服务器。 有关详细信息，请转到[配置 StorSimple 设备的 Web 代理](https://docs.microsoft.com/azure/storsimple/storsimple-8000-configure-web-proxy)。
* 确保根据 [StorSimple 设备的网络要求](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-requirements-for-your-storsimple-device)配置防火墙。
* 如果这不是你要在此服务中注册的第一个设备，请验证服务数据加密密钥是否正确。 此密钥是向 StorSimple 设备管理器服务注册第一个物理设备时获取的。

## <a name="recommended-documents"></a>**建议的文档**

[排查设备注册期间发生的错误](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#errors-during-device-registration)<br>
[使用用于 StorSimple 的 Windows PowerShell 管理设备](https://docs.microsoft.com/azure/storsimple/storsimple-8000-windows-powershell-administration)<br>
[获取服务注册密钥](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-service#get-the-service-registration-key)<br>
[StorSimple 设备的网络要求](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-requirements-for-your-storsimple-device)


<properties
    pageTitle="My device appears offline in the portal"
    description="设备在门户中显示为脱机"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="8000Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="my-device-appears-offline-in-the-portal"></a>设备在门户中显示为脱机。

如果设备已脱机，则无法与 StorSimple 设备管理器服务通信。 这可能是以下原因之一造成的：

## <a name="recommended-steps"></a>**建议的步骤**

* Internet 连接已断开。 在设备的 Windows PowerShell 界面中，运行 *Test-HcsmConnection*。 解决报告的问题。 有关详细信息，请转到[使用 Test-HcsmConnection cmdlet 进行故障排除](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#troubleshoot-with-the-test-hcsmconnection-cmdlet)。
* 一个或多个网络接口有问题。 运行 *Get-NetAdapter* cmdlet，检查网络接口的运行状况。 有关详细信息，请转到[使用 Get-NetAdapter cmdlet 进行故障排除](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#troubleshoot-with-the-get-netadapter-cmdlet)。
* 设备已关闭。 有关详细信息，请转到[打开 StorSimple 8000 系列设备](https://docs.microsoft.com/azure/storsimple/storsimple-turn-device-on-or-off)。
* Web 代理设置不正确。 有关详细信息，请转到[配置和查看设备的 Web 代理设置](https://docs.microsoft.com/azure/storsimple/storsimple-8000-configure-web-proxy)。
* 设备时间可能与 Internet 时间不同步。 检查时区和 NTP 服务器设置。 运行 *Sync-HcsTime*，在 NTP 服务器上强制设备时间同步。 有关详细说明，请转到[使用 Sync-HcsTime cmdlet 进行故障排除](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#troubleshoot-with-the-sync-hcstime-cmdlet)。

## <a name="recommended-documents"></a>**建议的文档**

[用于排查 StorSimple 部署问题的工具](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#tools-for-troubleshooting-storsimple-deployments)

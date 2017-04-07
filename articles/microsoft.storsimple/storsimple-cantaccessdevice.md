<properties
    pageTitle="I can’t access my device in File Explorer."
    description="我无法在文件资源管理器中访问我的设备。"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="9000Or1200Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-access-my-device-in-file-explorer"></a>我无法在文件资源管理器中访问我的设备。
如果你无法在文件资源管理器中访问你的设备，请执行以下操作。


## <a name="recommended-steps"></a>**建议的步骤**
1. 在虚拟阵列的本地 Web UI 中，转到**“疑难解答”** > **“诊断测试”**，然后单击**“运行诊断测试”**。
2. 如果你正在通过 IP 访问你的设备，请检查你是否使用了 DHCP 而不是静态 IP。 你的 IP 可能已更改。
3. 在 StorSimple 设备管理器的 Azure 门户中，转到“设备”边栏选项卡，并检查你的设备是否显示为已停用。
4. 检查 VM 的 Hyper-V 或 ESX 主机，确保 VM 已打开并正在运行。


## <a name="recommended-documents"></a>**建议的文档**
[通过本地 Web UI 进行故障排除](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[排查 Hyper-V 问题](https://technet.microsoft.com/library/cc742454.aspx)<br>
[排查 ESXi 服务器上的 VM 故障](https://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1003976)


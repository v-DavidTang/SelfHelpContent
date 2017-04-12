<properties
    pageTitle="I can’t access my shares or volumes."
    description="无法访问共享或卷。"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="10"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="9000Or1200Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-access-my-shares-or-volumes"></a>无法访问共享或卷。


## <a name="recommended-steps"></a>**建议的步骤**
1.  在虚拟阵列的本地 Web UI 中，转到**疑难解答** > **诊断测试**，然后单击**运行诊断测试**。 验证是否正确配置了设备，并解决报告的所有问题。
2. 在 StorSimple 设备管理器服务的 Azure 门户中，转到**卷**边栏选项卡。 选择相应的卷，使该卷脱机，然后使其重新联机。  如果使用文件服务器，请转到**共享**边栏选项卡，使共享脱机，然后使其重新联机
3. 如果使用文件资源管理器来访问共享，请右键单击共享文件夹名称，然后转到“属性” > “安全性”，以检查你是否有权访问该共享。
4. 如果刚刚启动了克隆并尝试访问目标共享/卷，该共享/卷可能尚未联机。 请稍候片刻，然后尝试对其进行访问。
5. 如果使用 iSCSI 服务器，请检查 iSCSI 发起程序配置，以确定该卷是否已连接。 如果卷未连接，请尝试连接。 如果连接卷失败，则可能是出现了云连接问题。
6. 如果这是你为此设备创建的的第一个共享，则可能会由于网络基础结构错误而导致无法进行 DNS 解析。
7. 请联系 Azure 支持人员，检查是否在云中造成了一定的延迟。

## <a name="recommended-documents"></a>**建议的文档**
[通过本地 Web UI 进行故障排除](https://aka.ms/storsimple-troubleshoot-diagnostics)


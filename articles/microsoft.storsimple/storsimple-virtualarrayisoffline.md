<properties
    pageTitle="My virtual array is offline"
    description="虚拟阵列已脱机"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 虚拟阵列已脱机
如果你的虚拟阵列已脱机，其原因可能是下列其中一项： <br>
1. 你的虚拟阵列可能已在虚拟机监控程序上关闭或暂停。 <br>
2. 你的虚拟阵列无法与 StorSimple 设备管理器服务通信。

## **建议的步骤**
1. 在虚拟阵列的本地 Web UI 中，转到**“疑难解答”** > **“诊断测试”**，然后单击**“运行诊断测试”**。
2. 你的虚拟阵列可能由于某项 Windows 更新而重新启动。 请等待几分钟，然后重试连接。
3. 如果用于存储快照或虚拟硬盘的卷上的可用存储空间不足，则在 Hyper-V 中，你的虚拟阵列将会暂停。 在 Hyper-V 管理器中，虚拟阵列的状态将列为*“已暂停 - 关键”*。 在该卷上腾出更多空间可以解决此问题。
4. 如果还是无法连接，请在 Hyper-V 主机或 ESX 服务器上检查，以确保 VM 运行状况正常。


## **建议的文档**
[通过本地 Web UI 进行故障排除](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[排查 Hyper-V 问题](https://technet.microsoft.com/en-us/library/cc742454.aspx)



<!--HONumber=Jul16_HO4-->



<properties
    pageTitle="I can't register my virtual array."
    description="无法注册虚拟阵列。"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="9000Or1200Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-register-my-virtual-array"></a>无法注册虚拟阵列。
如果注册失败，请执行以下操作。

## <a name="recommended-steps"></a>**建议的步骤**
1. 你的注册密钥可能不正确。 请验证你的注册密钥。 转到 [**管理** > **密钥**](data-blade:Microsoft_Azure_StorSimple.RegistrationKeyBlade) 来获取服务注册密钥。
2. 如果这不是你要在此服务中注册的第一个设备，请验证服务数据加密密钥是否正确。 在已注册到此服务的任何虚拟阵列的本地 Web UI 中，转到 **配置** > **云设置** ，然后单击 **获取服务数据加密密钥**。
3. 设备时间可能不同步。 在虚拟阵列的本地 Web UI 中，转到 **疑难解答** > **诊断测试** ，然后单击 **运行诊断测试**。 如果报告有时间偏差，请修改 NTP 服务器设置。
4. 代理服务器设置可能不正确。 在虚拟阵列的本地 Web UI 中，转到 **疑难解答** > **诊断测试** ，然后单击 **运行诊断测试**。 如果报告有差异，请更新代理服务器设置。


## <a name="recommended-documents"></a>**建议的文档**
[通过本地 Web UI 进行故障排除](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[获取服务注册密钥](https://aka.ms/storsimple-troubleshoot-registerkey)<br>
[StorSimple 虚拟阵列系统要求](https://aka.ms/storsimple-troubleshoot-va-reqs)


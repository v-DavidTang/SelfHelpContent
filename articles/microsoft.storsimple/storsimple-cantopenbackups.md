<properties
    pageTitle="I can’t open the backups in .backups folder."
    description="无法打开 .backups 文件夹中的备份。"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="8"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 无法打开 .backups 文件夹中的备份。
如果你无法打开 .backups 文件夹中的备份，请执行以下操作。


## **建议的步骤**
1. 在虚拟阵列的本地 Web UI 中，转到**“疑难解答”** > **“诊断测试”**，然后单击**“运行诊断测试”**。 解决报告的所有问题。
2. 确认你对尝试使用文件资源管理器访问的文件夹拥有权限。 右键单击文件夹名称，然后转到**“属性”** > **“安全性”**以查看权限。
3. 如果 .backups 文件夹中有 5 个以上的备份，则表示设备出现了暂时性的清理问题。 此问题将在几分钟后自行解决。 在看到只有 5 个剩余的备份文件后，请重试打开该文件夹。


## **建议的文档**
[通过本地 Web UI 进行故障排除](https://aka.ms/storsimple-troubleshoot-diagnostics)



<!--HONumber=Aug16_HO2-->



<properties
    pageTitle="Windows Backup to Azure Backup/Schedule backup for a Windows Server or a client"
    description="Windows 备份到 Azure 备份/计划 Windows Server 或客户端的备份"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="kasparks"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32447383"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# Windows 备份到 Azure 备份/计划 Windows Server 或客户端的备份

如果你遇到 Windows 服务器文件和文件夹备份速度缓慢的问题，请尝试执行以下一个或多个步骤

## **建议的步骤**

* 所备份的服务器存在性能限制，导致备份速度缓慢 <br>
[为获得最佳备份性能而要配置的性能计数器和建议的范围](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-slow-backup-performance-issue#cause1)

* 其他进程或防病毒软件干扰 Azure 备份，导致备份速度缓慢甚至失败 <br>
[确保不与其他进程或防病毒软件冲突的步骤](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-slow-backup-performance-issue/#cause2)

* 在 Azure IaaS VM 中备份单个文件和文件夹时速度缓慢 <br>
[优化 Azure VM 性能的步骤](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-slow-backup-performance-issue/#cause3)

* 备份大量（数百万个）小型文件时速度缓慢 <br>
[识别备份大量文件时存在的瓶颈的步骤](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-slow-backup-performance-issue/#cause4)

## **建议的文档**
[使用 Azure 备份代理设置文件和文件夹备份的分步指南](https://azure.microsoft.com/en-us/documentation/articles/backup-configure-vault/)



<!--HONumber=Aug16_HO2-->



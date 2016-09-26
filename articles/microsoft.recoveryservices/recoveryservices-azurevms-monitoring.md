<properties
    pageTitle="Azure virtual machine backup monitoring and reporting issues"
    description="Azure 虚拟机备份监视和报告问题"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="saurabhsensharma"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds="32447361"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>



# Azure 虚拟机备份监视和报告问题

## **建议的步骤**
尝试下面建议的步骤，解决常见的 Azure IaaS VM 备份监视和报告问题

* 请注意，只会针对失败的备份引发警报

* 如果电子邮件未进入收件箱，请查看垃圾邮件文件夹

* 是否存在即使配置了通知，也不发送电子邮件的情况？ 在以下情况下不会引发警报，也不会发送电子邮件，目的是减少干扰性警报<br>
    1. 如果已将通知配置为“每小时摘要”，并且在一小时内引发并解决了警报 <br>
    2. 取消了作业 <br>
    3. 某个备份作业被触发但随后失败，而另一个备份作业正在进行 <br>
    4. 为启用 Resource Manager 的 VM 启动了计划的备份作业，但该 VM 不再存在 <br>

##**建议的文档**

 [Azure 虚拟机备份监视指南](https://azure.microsoft.com/documentation/articles/backup-azure-monitor-vms/)<br>



<!--HONumber=Sep16_HO3-->



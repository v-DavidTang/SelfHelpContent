
<properties
    pageTitle="Azure Linux VM Restore Limitations"
    description="从备份还原 Azure VM 时的限制"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="trinadhk"
    displayOrder="9"
    selfHelpType="resource"
    supportTopicIds="32553297"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# <a name="azure-linux-vm-restore-limitations"></a>Azure Linux VM 还原限制

## <a name="limitations-when-restoring-a-vm"></a>**还原 VM 时的限制**
从备份还原 Linux Azure VM 时，将应用以下限制。 

* 不支持在恢复过程中替换现有虚拟机。 请从备份创建新的虚拟机，或从备份还原磁盘并使用磁盘进行配置来创建新的 VM。

* 不支持跨区域和跨订阅还原，即如果在西欧备份 VM，则只能将其还原到同一订阅中的西欧。 

* 对于域控制器 VM，建议使用“还原磁盘”，并从还原的磁盘创建新的 VM。 

* 建议为 Linux VM 使用基于 SSH 的身份验证。 如果在备份的 VM 上使用基于密码的身份验证，则还原后需使用 VM 访问扩展[重置密码](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-classic-reset-access/)。 

* 若要将 VM 还原到特定的可用性集，还原磁盘和配置，并使用 PowerShell cmdlet 创建 VM。 [了解详细信息](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm)

* 如果还原虚拟机时出现问题，请尝试还原磁盘并使用还原的磁盘创建虚拟机。

* 还原磁盘将还原所有磁盘（附加到 VM 的 OS 和数据磁盘）。 使用此选项无法还原单个磁盘。 

* 如果出现 Azure 数据中心灾难，Azure 备份在配对的数据中心中还原 VM。 [了解详细信息](https://docs.microsoft.com/azure/backup/backup-azure-restore-vms#restoring-a-vm-during-azure-datacenter-disaster)

## <a name="recommended-documents"></a>**建议的文档**
[Azure 虚拟机还原疑难解答指南](https://docs.microsoft.comazure/backup/backup-azure-vms-troubleshoot/)<br>
[如何使用门户还原虚拟机](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)<br>
[如何使用 PowerShell 还原虚拟机](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm)



<!--HONumber=Dec16_HO1-->



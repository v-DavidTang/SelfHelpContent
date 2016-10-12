<properties
    pageTitle="How to delete a Recovery Services vault or Backup vault"
    description="无法删除备份保管库或恢复服务保管库"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="anuragm"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# 删除存储所有备份数据的保管库
有两种类型的保管库 - 用于 Resources Manager 部署的恢复服务保管库，以及用于经典部署的备份保管库。
## **建议的步骤**
### **删除恢复服务保管库**
1. 打开 Azure 门户，然后选择要删除的保管库。
2. 在保管库视图中查看概要窗格，确保“备份项”、“备份管理服务器”和“复制的项”下的所有条目均为零。 如果看到非零值，请遵循[删除恢复服务保管库中的所有资源的步骤](https://azure.microsoft.com/documentation/articles/backup-azure-delete-vault/#deleting-a-recovery-services-vault)。
3. 当保管库中没有其他项时，请单击“删除”。
4. 当系统询问是否确定要删除保管库时，请单击“是”。
随即会删除该保管库，门户返回“新建服务”菜单。

### **删除备份保管库**
1. 打开经典门户，然后选择要删除的保管库。
2. 查看与保管库关联的 Windows 服务器和/或 Azure 虚拟机数以及消耗的存储空间总数，确保使用量为零。 如果看到非零值，请遵循[删除备份保管库中的所有资源的步骤](https://azure.microsoft.com/documentation/articles/backup-azure-delete-vault/#delete-a-backup-vault)。
3. 如果使用量为零，请单击“删除”。
4. 选择删除该保管库的原因选项，然后单击复选标记。
随即会删除该保管库，并返回到经典门户仪表板。

## **建议的文档**
[删除 Azure 备份保管库](https://azure.microsoft.com/documentation/articles/backup-azure-delete-vault/)<br>
[Azure 备份常见问题](https://azure.microsoft.com/documentation/articles/backup-azure-backup-faq/)<br>




<!--HONumber=Sep16_HO5-->



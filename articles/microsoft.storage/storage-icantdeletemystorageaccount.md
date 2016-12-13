<properties
    pageTitle="I can't delete my storage account"
    description="无法删除存储帐户"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="passaree"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32551644,32551656,32551657,32551665"
    resourceTags=""
    productPesIds="15629"
    cloudEnvironments="public"
/>


# <a name="i-cant-delete-my-storage-account"></a>无法删除存储帐户

## <a name="recommended-steps"></a>**建议的步骤**
当你尝试在 Azure 门户或 Azure 经典门户中删除 Azure 存储帐户、容器或 VHD 时，可能会收到错误。 这些问题可能是由以下情况造成的：

- 当你删除 VM 时，磁盘和 VHD 未自动删除。 这可能是存储帐户删除失败的原因。 我们不会删除磁盘，以便你可以使用该磁盘装入另一个 VM。<br>
- 磁盘或者与磁盘关联的 Blob 上仍有租约。<br>

如果存储帐户使用 ARM 部署模型，你可以执行以下步骤来删除 VHD：

1. 转到“存储帐户”|“Blob”|“VHD”，找到想要删除的 VHD，或者导致无法删除容器或存储帐户的 VHD。  单击此 VHD 时，它会显示为“已锁定”/“已租用”。
2. 确定哪个 VM 当前正在使用已租用的 VHD。  通常，VHD 的名称包含 VM 的名称。
3. 转到租用该 VHD 的 VM 所对应的“虚拟机”|“磁盘”。  
4. 从该 VM 中删除该 VHD 即可。  对于 OS 磁盘，需要删除正在使用该磁盘的 VM。  对于数据磁盘，请单击该磁盘，然后选择“分离”。


## <a name="recommended-documents"></a>**建议的文档**
[删除存储帐户时出现问题](https://azure.microsoft.com/documentation/articles/storage-resource-manager-cannot-delete-storage-account-container-vhd/)



<!--HONumber=Nov16_HO4-->



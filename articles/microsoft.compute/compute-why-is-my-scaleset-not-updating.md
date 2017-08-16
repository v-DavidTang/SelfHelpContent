<properties
    pageTitle="Why is my scale set not updating"
    description="我的规模集为何不更新"
    service="microsoft.compute"
    resource="virtualmachinescalesets"
    authors="gatneil"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>


# <a name="why-is-my-scale-set-not-updating"></a>我的规模集为何不更新

更新规模集时，如果正在运行的 VM 未更新，原因可能是升级策略模式设置为“手动”。 在此模式下，对规模集所做的更改会立即应用到新 VM，但是，仅当在现有 VM 上调用手动升级时，这些更改才会应用到现有 VM。 可以编程方式或者通过 Azure 门户中规模集的“实例”边栏选项卡应用更改。 如果想要同时对规模集中的所有 VM 自动应用更新，可将升级策略模式改为“自动”。

## <a name="recommended-documents"></a>建议的文档

有关更新规模集的详细信息，请参阅[此文档](https://docs.azure.cn/zh-cn/virtual-machine-scale-sets/virtual-machine-scale-sets-deploy-app)，其中介绍了如何在规模集上部署、管理和升级应用。




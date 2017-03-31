<properties
    pageTitle="Why would you ever create a scale set with fewer than 2 VMs"
    description="为何创建包含 2 个以下 VM 的规模集"
    service="microsoft.compute"
    resource="virtualmachinescalesets"
    author="gatneil"
    displayOrder="49"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>


# <a name="why-would-you-ever-create-a-scale-set-with-fewer-than-2-vms"></a>为何创建包含 2 个以下 VM 的规模集

创建包含 2 个以下 VM 的规模集的原因是什么？


原因之一是利用规模集的弹性属性。 例如，可以部署不包含任何 VM 的规模集来定义基础结构，这样就无需支付 VM 运行费。 然后，在准备好部署 VM 时，可将规模集的“容量”提高到生产实例计数。

另一个原因是要对规模集执行某项操作，同时不关心可用性，就如同在离散的 VM 中使用可用性集的情况一样。 此外，可以借助规模集来使用可替代的无差别计算单位。 这种一致性是规模集相比可用性集存在的一项重要优势。 许多无状态工作负载不关心单个单位，可以在工作负荷下降时缩减为一个计算单位，在工作负荷提高时扩展回到多个计算单位。

请参阅[本文档](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-portal-create)以了解如何从门户部署规模集。


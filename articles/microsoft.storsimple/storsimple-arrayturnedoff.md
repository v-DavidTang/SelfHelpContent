<properties
    pageTitle="My virtual array has turned off"
    description="我的虚拟阵列已关闭"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="9000Or1200Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="my-virtual-array-has-turned-off"></a>我的虚拟阵列已关闭。
这可能是以下原因之一造成的：

## <a name="recommended-steps"></a>**建议的步骤**
1. 预配虚拟阵列的主机上的磁盘空间已耗尽。 如果你正在运行 Hyper-V，请执行以下操作来腾出更多的空间：<br>
    1. 启动 Hyper-V 管理器。 转到**“工具”** > **“服务器管理器”** > **“Hyper-V 管理器”**。<br>
    2. 在**“虚拟机”**列表中，找到状态为 `Paused-Critical` 的虚拟阵列。<br>
    3. 释放资源，以便可以启动虚拟阵列。 例如，可以释放相应硬盘驱动器上的磁盘空间。<br>
    4. 右键单击每个虚拟阵列，然后单击**“恢复”**。 这会将虚拟机返回到运行状态。<br>
2. 如果虚拟阵列上的磁盘空间未耗尽，请尝试将其打开。


## <a name="recommended-documents"></a>**建议的文档**
[排查 Hyper-V 问题](https://technet.microsoft.com/library/cc742454.aspx)<br>
[排查 ESXi 服务器上的 VM 故障](https://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&externalId=1003976)


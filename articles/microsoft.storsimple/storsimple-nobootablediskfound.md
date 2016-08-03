<properties
    pageTitle="My virtual array isn't booting"
    description="我的虚拟阵列不启动"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 我的虚拟阵列不启动。
如果由于磁盘问题而无法启动 Hyper-V 虚拟阵列。 检查所用的虚拟磁盘映像版本。 <br>
常见错误消息： <br>
    1. `Boot failure. Reboot and Select proper Boot device`<br>
    2. `Insert Boot Media in selected Boot device`

## **建议的步骤**
* 如果使用适用于 Windows Server 2008 R2 或更高版本的 VHD，则需要创建**第 1 代** VM。
* 如果使用适用于 Windows Server 2012 或更高版本的 VHDX，则需要创建**第 2 代** VM。


## **建议的文档**
[在 Hyper-V 中预配虚拟阵列。](https://aka.ms/storsimple-troubleshoot-provisionarray)<br>
[适用于 Hyper-V 2008 R2 和更高版本的 VHD](https://go.microsoft.com/fwLink/?LinkID=692085&clcid=0x409)<br>
[适用于 Hyper-V 2012 和更高版本的 VHDX](https://go.microsoft.com/fwLink/?LinkID=724278&clcid=0x409)<br>
[第 2 代虚拟机概述](https://technet.microsoft.com/en-us/library/dn282285.aspx)



<!--HONumber=Jul16_HO4-->



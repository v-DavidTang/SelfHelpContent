<properties
    pageTitle="站点恢复（VMware 到 Azure）/故障转移后重新保护 VM"
    description="站点恢复（VMware 到 Azure）/故障转移后重新保护 VM"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536447"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# 站点恢复（VMware 到 Azure）/故障转移后重新保护 VM

故障回复或重新保护过程中常见的问题
## **建议的步骤**

* 用于发现的 vCenter 帐户应有适当的故障回复权限 <br>
[请参阅此处的权限列表](https://aka.ms/asrsupfailbackperm)

* vCenter 许可证不应是免费许可证，而应是“评估”或“已许可”。 <br>
在 vCenter 中的 ESXi 主机节点上，导航到“配置”选项卡 ->“许可的功能”。 vSphere API 应列在产品功能下面。故障转移的 VM 应在正确的网络中

* VM 应该正在运行并在网络中才能与配置服务器和进程服务器通信。 <br>
检查 VM 是否在已附加到 Azure 网络的 ExpressRoute 或 VPN 中。

* 应将包含 VM 磁盘的数据存储装载到主目标 ESXi 主机 <br>
确保将数据存储装载为读写存储，并采用 VMFS 类型。 当前不支持其他数据存储类型。

* 如果选择菜单中未出现保留驱动器，请将一个新驱动器添加到主目标<br>
    1. 卷不应用于任何其他目的（复制的目标，等等）
    2. 卷不应处于锁定模式。
    3. 卷不应为缓存卷。 （该卷上不应存在 MT 安装。 PS+MT 自定义安装卷不能用作保留卷。 此处安装的 PS+MT 卷是 MT 的缓存卷。 ）
    4. 卷文件系统类型不应为 FAT 和 FAT32。
    5. 卷容量应为非零值。 e. Windows 的默认保留卷是 R 卷。
    6. Linux 的默认保留卷是 /mnt/retention。

* [此处还列出了一些常见问题](https://aka.ms/asrsupfailbackcommonissues)

## **建议的文档**
[此处](https://aka.ms/asrsupv2afailback)提供了端到端故障回复文档



<!--HONumber=Jul16_HO4-->



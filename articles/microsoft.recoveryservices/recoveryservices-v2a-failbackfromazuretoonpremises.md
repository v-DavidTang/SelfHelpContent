<properties
    pageTitle="Site Recovery (VMware to Azure)/Failback from Azure to on-premises"
    description="站点恢复（VMware 到 Azure）/从 Azure 故障回复到本地"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536408"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# <a name="site-recovery-vmware-to-azurefailback-from-azure-to-on-premises"></a>站点恢复（VMware 到 Azure）/从 Azure 故障回复到本地

故障回复或重新保护过程中常见的问题
## <a name="recommended-steps"></a>**建议的步骤**

* 故障回复需要站点到站点 VPN 或对专用对等互联的快速路由。进行故障回复前，需确保站点到站点的 VPN 可用，这样 Azure 中故障转移的 VM 才能瞄准本地配置服务器。 仅可通过 VPN/ER（专用对等互联）进行从 Azure 到本地的复制。 有关更多详细信息，请查看[故障回复文档](https://aka.ms/asrsupv2afailback)。

* 不应在主目标上启用存储 vMotion <br>
启动虚拟机可能失败并出现类似于“VMware ESX 找不到虚拟磁盘 "DRIVE0.vmdk"。 请验证路径是否有效，然后重试”的错误。 你可以在数据存储中查找磁盘并将其附加到 VM，然后，VM 将成功启动。

* 用于发现的 vCenter 帐户应有适当的故障回复权限 <br>
[请参阅此处的权限列表](https://aka.ms/asrsupfailbackperm)

* vCenter 许可证不应是免费许可证，而应是“评估”或“已许可”。 <br>
在 vCenter 中的 ESXi 主机节点上，导航到“配置”选项卡 ->“许可的功能”。 vSphere API 在产品功能中列出


* 应将包含 VM 磁盘的数据存储装载到主目标 ESXi 主机<br>
确保将数据存储装载为读写存储，并采用 VMFS 类型。 当前不支持其他数据存储类型。

* 如果选择菜单中未出现保留驱动器，请将一个新驱动器添加到主目标 <br>
    1. 卷不应用于任何其他目的（复制的目标，等等）
    2. 卷不应处于锁定模式。
    3. 卷不应为缓存卷。 （该卷上不应存在 MT 安装。 PS+MT 自定义安装卷不能用作保留卷。 此处安装的 PS+MT 卷是 MT 的缓存卷。 ）
    4. 卷文件系统类型不应为 FAT 和 FAT32。
    5. 卷容量应为非零值。 e. Windows 的默认保留卷是 R 卷。
    6. Linux 的默认保留卷是 /mnt/retention。


* [此处还列出了一些常见问题](https://aka.ms/asrsupfailbackcommonissues)

## <a name="recommended-documents"></a>**建议的文档**

          [此处](https://aka.ms/asrsupv2afailback)提供了端到端故障回复文档



<!--HONumber=Dec16_HO1-->



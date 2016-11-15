<properties
    pageTitle="Site Recovery (VMware to Azure)/Enable Protection"
    description="站点恢复（VMware 到 Azure）/启用保护期间出现的常见问题"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536405"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# <a name="site-recovery-vmware-to-azureenable-protection"></a>站点恢复（VMware 到 Azure）/启用保护

启用复制期间出现的常见问题

## <a name="recommended-steps"></a>**建议的步骤**

* 确保使用容量计划工具来避免复制内容遗漏和不符合 SLA<add link>

* 确保要保护的服务器满足以下要求
    -   每个磁盘的大小应小于 1TB
    -   OS 磁盘应是基本磁盘而不是动态磁盘
    -   服务器的名称应符合 Azure 虚拟机名称要求 – 长度不应小于 16 个字符，且包含字母数字、下划线和连字符。 有关详细信息，请参阅 http://aka.ms/asrstnaming
    -   未[启用 UEFI](http://aka.ms/asrstuefi)
* **无法使用 Azure Site Recovery 保护**以下 Azure Site Recovery 基础结构服务器
 - 配置服务器
 - 横向扩展进程服务器
 - 主目标服务器（Windows 和 Linux）
* 确保服务器上已安装移动服务。 如果你选择推送安装，则必须满足以下要求：在要保护的计算机的 Windows 防火墙上，选择“允许应用或功能通过防火墙”。 启用“文件和打印机共享”和“Windows Management Instrumentation”。 对于属于某个域的计算机，可以使用 GPO 配置防火墙设置。

* 选择一个有效的存储帐户。 不支持 RA-GRS 类型和 Blob 类型的存储帐户。

* 确保操作系统符合要求。

* 确保传递的帐户凭据对计算机拥有管理员权限。

## <a name="recommended-documents"></a>**建议的文档**
[VMware 到 Azure](aka.ms/asrstv2a)



<!--HONumber=Nov16_HO2-->



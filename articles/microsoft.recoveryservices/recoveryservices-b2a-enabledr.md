<properties
    pageTitle="Site Recovery (Hyper-V Site to Azure)/Enable Protection"
    description="站点恢复（Hyper-V 站点到 Azure）/启用保护期间出现的常见问题"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536401"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# 站点恢复（Hyper-V 站点到 Azure）/启用保护

启用复制期间出现的常见问题

## **建议的步骤**

* 确保使用容量计划工具来避免复制内容遗漏和不符合 SLA

* 确保要保护的服务器满足以下要求
    -   每个磁盘的大小应小于 1TB
    -   OS 磁盘应是基本磁盘而不是动态磁盘
    -   服务器的名称应符合 Azure 虚拟机名称要求 – 长度不应小于 16 个字符，且包含字母数字、下划线和连字符。 有关详细信息，请[参阅此文](http://aka.ms/asrstnaming)

* 对于第 2 代虚拟机/已启用 UEFI 的虚拟机，操作系统系列应是 Windows，并且启动盘应小于 300GB。

* 选择一个有效的存储帐户。 不支持 RA-GRS 类型和 Blob 类型的存储帐户。

* Hyper-V 服务器上应已安装[文章 2961977](https://support.microsoft.com/kb/2961977) 中提到的修补程序。
## **建议的文档**
[Hyper-V 站点到 Azure](http://aka.ms/asrstb2a)


<!--HONumber=Aug16_HO3-->



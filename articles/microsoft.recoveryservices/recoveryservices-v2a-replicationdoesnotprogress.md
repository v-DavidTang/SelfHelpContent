<properties
    pageTitle="Site Recovery (VMware to Azure)/Replication does not progress"
    description="Site Recovery（VMware 到 Azure）/在复制期间出现的常见问题"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536441"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# <a name="site-recovery-vmware-to-azurereplication-does-not-progress"></a>Site Recovery（VMware 到 Azure）/复制无法进行

在复制期间出现的常见问题

## <a name="recommended-steps"></a>**建议的步骤**

**复制速度缓慢/数据上载速度受限**

如果看到复制对进展速度缓慢，请确保有足够的带宽。

- **超过阈值的缓存文件夹**警报意味着正在达到用于复制的进程服务器缓存的默认阈值限制。这在初始复制期间或在发生高改动期间十分常见，如果有足够的带宽，这种情况应会消失。
- 使用 [ASR Capacity Planner](https://aka.ms/asr-capacity-planner-doc) 可计算复制所需的带宽 
- [配置最大上载线程限制](https://aka.ms/max-thread-upload)可影响带宽流量。 

**复制停滞**

- 请确保配置服务器上的入站端口 443 未被阻止。 可以使用 Telnet 检查它。 [阅读有关配置服务器先决条件的详细信息](https://aka.ms/selfhelp_csprereqs) 
- 请确保按照针对 ASR 的[防病毒建议](https://aka.ms/asr-antivirus)执行操作。
- 如果发生字节读取错误，请通过在只读模式下运行 chkdsk（对于 linux，则运行 dd），确保源磁盘上的任何扇区未损坏。 在使用 chkdsk 修复错误后禁用/启用保护。 
- 请确保正在保护的不是克隆服务器。
- 请确保代理（如果有）已正确设置

**数据上载被阻止**

* 请确保源计算机与进程服务器之间存在网络连接
- 如果使用的是 VPN 连接，请确保建立了连接
- 检查源服务器上是否正在运行移动服务（InMage Scout VX 代理 - Sentinel/Outpost、InMage Scout 应用程序服务）

## <a name="recommended-documents"></a>**建议的文档**
[VMware 到 Azure](http://aka.ms/asrstv2a)



<!--HONumber=Nov16_HO5-->



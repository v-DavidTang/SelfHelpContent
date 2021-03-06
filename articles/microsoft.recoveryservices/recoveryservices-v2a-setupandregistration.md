<properties
    pageTitle="Site Recovery (VMware vCenter to Azure)/Add/register configuration server"
    description="站点恢复（VMware vCenter 到 Azure）/添加/注册配置服务器"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="anoopkv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32536387"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>

# <a name="site-recovery-vmware-vcenter-to-azureaddregister-configuration-server"></a>站点恢复（VMware vCenter 到 Azure）/添加/注册配置服务器

安装和注册配置服务器过程中出现的常见问题

## <a name="recommended-steps"></a>**建议的步骤**
* 确保安装**配置服务器**的服务器有权访问以下 URL <br>
    1. \*.hypervrecoverymanager.windowsazure.com
    2. \*.accesscontrol.windows.net
    3. \*.backup.windowsazure.com
    4. \*.blob.core.windows.net
     5. \*.store.core.windows.net
    6. time.nist.gov
    7. time.windows.com
    8. https://dev.mysql.com/get/archives/mysql-5.5/mysql-5.5.37-win32.msi

* 确保安装**配置服务器**的服务器上的时钟已根据其目标时区设置了正确的时间。

* 如果你知道要安装**配置服务器**的服务器在代理服务器后面，请确保选择**“使用代理服务器连接到 Azure Site Recovery”**选项。<br>
    1. 随时可以通过运行 **CSPSConfigtool.exe** 并重新注册 Microsoft Azure Site Recovery 提供程序来更改此设置。
    2. 可以在配置服务器中的 [安装位置]\home\svsystems\bin 文件夹下找到 **CSPSConfigtool.exe**。

* 确保你打算在其上安装配置服务器的服务器上已安装 PowerCLI 版本 6.0。<br>
    1. 不支持更高/更低的 PowerCLI 版本。
    2. 可以从 https://developercenter.vmware.com/tool/vsphere_powercli/6.0 下载 PowerCLI 6.0

* 确保没有为运行安装程序的用户启用以下组策略。<br>
    1. 阻止访问命令提示符
    2. 阻止访问注册表编辑工具
    3. 文件附件的信任逻辑
    4. 打开脚本执行

* 确保要安装**配置服务器**的服务器上已启用 TLS1.0。

* 确保安装**配置服务器**的计算机上未针对 IIS 服务进行以下配置。<br>
    1. 已配置多个网站
    2. 已配置 FastCGISettings
    3. 端口 443 已绑定为“默认网站”安全端口
    4. 已禁用匿名身份验证

* 如果成功注册**配置服务器**后无法发现 vCenter，请确保运行**配置服务器**的计算机上未安装其他 Perl 或 PHP 版本

## <a name="recommended-documents"></a>**建议的文档**
* [配置服务器硬件和软件先决条件](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#prerequisites)
* [安装和注册配置服务器](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#installing-and-registering-a-configuration-server-from-gui)
* [如何将配置服务器注册到不同的保管库](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#registering-a-configuration-server-with-a-different-recovery-services-vault)
* [续订配置服务器 SSL 证书](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#renew-configuration-server-secure-socket-layerssl-certificates)
* [修改配置服务器的代理设置](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#modifying-proxy-settings-for-configuration-server)
* [缩放配置服务器的限制](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#sizing-requirements-for-a-configuration-server)
* [对配置服务器解除授权](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#decommissioning-a-configuration-server)



<!--HONumber=Feb17_HO4-->



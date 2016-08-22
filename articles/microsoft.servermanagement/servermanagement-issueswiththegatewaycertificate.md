<properties
    pageTitle="Issues with the gateway certificate"
    description="如何解决网关证书问题"
    service="microsoft.servermanagement"
    resource="gateways"
    authors="samli"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 网关证书问题

## **建议的步骤**
证书要求可能会改变，或者证书可能会过期。 若要解决此问题，请尝试以下解决方法之一：

* 使用网关安装程序注册新证书。 需要重新输入以前保存的凭据。
  1. 在网关计算机上，转到“程序和功能”并卸载“Server 管理工具网关”。
  2. [生成新的网关部署包](data-blade:Microsoft_Azure_RSMT.GatewaySetupBlade)，然后下载该包并将它安装在网关计算机上。 在安装过程中，请选择新的自签名证书或现有的已安装证书。
  3. 如果你保存了用于连接的凭据，可以使用“管理方式”再次输入凭据，因为新证书无法解密以前保存的凭据。
* 使用证书轮转脚本来注册新证书。 以前保存的凭据将继续工作。
  1. 在网关计算机上，以管理员权限打开 PowerShell。
  2. 将目录切换到安装网关软件的文件夹，例如 Scripts `C:\Program Files\ServerManagementToolsGateway\Scripts`
  3. 运行不带参数的 `New-GatewayEncryptionCert.ps1` 以生成新的自签名证书，或结合 `-Thumbprint <thumbprint>` 参数运行该命令以使用现有的已安装证书。
  4. 重新启动网关服务。 如果已保存用于连接的凭据，则在证书轮转期间（当前为 30 天）当你访问连接时，这些凭据至少可正常使用一次，这样，便可以使用新证书重新加密以前保存的凭据。



<!--HONumber=Aug16_HO3-->



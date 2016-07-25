<properties
    pageTitle="I can’t set up a connection to a Windows Server 2012 or 2012 R2 machine"
    description="无法与 Windows Server 2012 或 2012 R2 计算机建立 Server 管理工具连接"
    service="microsoft.servermanagement"
    resource="nodes"
    authors="jol"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 无法与 Windows Server 2012 或 2012 R2 计算机建立连接

## **建议的步骤**
若要使用 Server 管理工具连接到 Windows Server 2012 或 2012 R2 计算机，需要另外安装 WMI 提供程序包和 Windows Management Framework 5.0。 使用 Server 管理工具连接到服务器时，该工具将会检测这些包并提示你是否要安装。 如果在安装包时发生错误，或者在安装包后无法连接到服务器，请尝试以下一种或多种方法。

* 检查网关计算机上的安装日志<br>
检查**网关计算机**上的 WMI 和 WMF 安装日志，以查看任何错误或详细信息。 这些日志是进行故障排除时参考的第一手资料，可在以下路径中找到。 WMI 安装日志位于 Providers 子文件夹中，WMF 安装日志位于 WMF5 子文件夹中。<br>
**%windir%\ServiceProfiles\NetworkService\AppData\Local\Temp\Logs\ServerManagementPrerequisites**
* 检查目标计算机上的安装日志<br>
如果需要参考更详细的日志以进行高级故障排除，请检查**目标计算机**上的 WMI 和 WMF 安装日志。<br>
**%systemdrive%\SMTInstallers\Logs**
* 目标计算机上发生 WinRM 错误<br>
如果安装包之后或者在连接到 Windows Server 2012 或 2012 R2 计算机时发生以下错误，请登录到目标计算机上，并运行“services.msc”以启动“服务”MMC 管理单元。 然后重新启动“Windows 远程管理(WS-Management)”服务。<br>
**“WinRM 客户端接收到 HTTP 服务器错误状态(500)，但远程服务并未包含有关失败原因的任何其他信息”**
* 如果尝试了上述所有步骤但仍然无法连接到目标计算机，请参阅上面的“无法连接到服务器”部分中所述的其他故障排除步骤。




<!--HONumber=Jul16_HO3-->



<properties
    pageTitle="I can’t connect to a server"
    description="无法连接到 Server 管理工具节点"
    service="microsoft.servermanagement"
    resource="nodes"
    authors="jol"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 无法连接到服务器

## **建议的步骤**
若要解决常见问题，请尝试下面的一种或多种方法。

* 检查网关的运行状况<br>
确保“网关”边栏选项卡中的“运行状况”状态显示为“正常”。 如果不正常，请参阅“网关”边栏选项卡的“排除故障”菜单中的“无法连接到网关”部分。
* 连接到未加入域的工作组计算机<br>
如果你要尝试连接到工作组计算机，请在网关计算机上的 PowerShell 中或命令提示符下以管理员身份运行以下命令。 **TargetMachineIPAddress** 应是要连接到的工作组计算机的 IP 地址。 此外，在与工作组计算机建立 Server 管理工具连接时，请使用计算机的 IP 地址作为计算机名。<br>
**winrm set winrm/config/client @{ TrustedHosts="TargetMachineIPAddress" }**
* 使用本地用户帐户登录<br>
在服务器连接的“管理方式”对话框中输入凭据时，若要使用属于本地管理员组的本地用户帐户，需要在目标计算机上的 PowerShell 中或命令提示符下以管理员身份运行以下命令，以便在目标计算机上启用策略：<br>
**REG ADD HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v LocalAccountTokenFilterPolicy /t REG_DWORD /d 1**
* 连接到其他子网中的工作组计算机<br>
若要连接到与网关不在同一子网中的工作组计算机，请确保目标计算机上的 WinRM 防火墙端口 (TCP 5985) 允许入站流量。 可以在目标计算机上的 PowerShell 中或命令提示符下以管理员身份运行以下命令，以创建此防火墙规则：<br>
**NETSH advfirewall firewall add rule name="WinRM 5985" protocol=TCP dir=in localport=5985 action=allow**<br><br>
[Windows 远程管理 - 从远程计算机获取数据](https://msdn.microsoft.com/en-us/library/aa384423.aspx)
* 连接到服务器时出现“无法连接”错误<br>
如果在“管理方式”弹出式对话框中输入凭据时遇到“无法连接”错误，请确保凭据正确，并且用户是目标服务器的本地管理员组的成员。 在某些情况下，WinRM 还额外要求用户是“远程管理用户”组的成员。
* 连接到 Windows Server 2012 或 2012 R2 计算机<br>
在配置 Windows Server 2012 或 2012 R2 计算机的连接时，如果遇到“未检测到所需的软件”错误，或者在安装所需的包时遇到问题，请参阅下面的“无法与 Windows Server 2012 或 2012 R2 计算机建立连接”部分。

## **建议的文档**
[Server 管理工具简介](https://blogs.technet.microsoft.com/nanoserver/2016/02/09/introducing-server-management-tools/)



<!--HONumber=Jul16_HO3-->



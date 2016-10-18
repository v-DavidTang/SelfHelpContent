<properties
    pageTitle="I can’t connect to a server"
    description="无法连接到 Server 管理工具节点"
    service="microsoft.servermanagement"
    resource="nodes"
    authors="danielleemsft"
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

* 网关的运行状态是否显示为“正常”？<br>
在 Server 管理工具连接边栏选项卡中，转到“概述”菜单，检查“概要”部分中的“网关名称”，确保显示为“正常”。 如果未显示“正常”，请单击“网关名称”打开“网关”边栏选项卡，然后查看有关错误的详细信息。 也可以在“网关”边栏选项卡上的“诊断和解决问题”菜单中查找常见网关问题的解决方法。
* 目标服务器是否为工作组（未加入域）计算机？<br>
如果是，需要将目标服务器添加到网关计算机上的“受信任主机”列表。 在网关计算机上的 PowerShell 中或命令提示符下以管理员身份运行以下命令。 `TargetMachineNameOrAddress` 应该是在 Azure 中创建 Server 管理工具连接时使用的 NetBIOS 名称、FQDN 或 IP 地址（IPv4 或 IPv6）（也是边栏选项卡顶部显示的名称）。 还可以添加多台计算机，用逗号分隔即可。<br>
**命令提示符：** `winrm set winrm/config/client @{TrustedHosts=”TargetMachineNameOrAddress”}`<br>
**PowerShell：** `winrm set winrm/config/client ‘@{TrustedHosts=”TargetMachineNameOrAddress”}’`<br>
**注意：**上述命令会将任何现有的受信任主机列表替换为命令中指定的主机。 可以在 PowerShell 中结合 `Concatenate` 参数使用以下命令，将计算机名称添加到现有的受信任主机列表。<br>
`Set-Item wsman:\localhost\Client\TrustedHosts TargetMachineNameOrAddress –Concatenate`
* 连接时是否使用了本地用户帐户？<br>
在服务器连接的“管理方式”对话框中输入凭据时，可以使用属于目标服务器上本地管理员组的本地帐户或域帐户。 使用不属于内置管理员帐户的本地用户帐户时，需要在目标计算机上的 PowerShell 中或命令提示符下以管理员身份运行以下命令，在目标计算机上启用策略。<br>
`REG ADD HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v LocalAccountTokenFilterPolicy /t REG_DWORD /d 1`
* 连接的是否为其他子网中的工作组计算机？<br>
若要连接到与网关不在同一子网中的工作组计算机，请确保目标计算机上的 WinRM 防火墙端口 (TCP 5985) 允许入站流量。 可以在目标计算机上的 PowerShell 中或命令提示符下以管理员身份运行以下命令，以创建此防火墙规则：<br>
`NETSH advfirewall firewall add rule name=”WinRM 5985″ protocol=TCP dir=in localport=5985 action=allow`
* 连接到服务器时出现“无法连接”错误<br>
如果在“管理方式”弹出式对话框中输入凭据时遇到“无法连接”错误，请确保凭据正确，并且用户是目标服务器的本地管理员组的成员。 在某些情况下，WinRM 还额外要求用户是“远程管理用户”组的成员。
* 是否仅当连接到 Windows Server 2012 或 2012 R2 计算机时才出现问题？<br>
如果可以连接到 Windows Server 2016 计算机，但无法连接到 2012 或 2012 R2 计算机，请查看下面的“无法与 Windows Server 2012 或 2012 R2 计算机建立连接”部分。

## **建议的文档**
[Server 管理工具设置指南](https://blogs.technet.microsoft.com/servermanagement/2016/08/17/deploy-setup-server-management-tools/)



<!--HONumber=Oct16_HO1-->



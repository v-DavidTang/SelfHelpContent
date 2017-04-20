<properties
    pageTitle="How do I reset the password or ssh key on my scale set VMs"
    description="如何重置规模集 VM 上的密码或 SSH 密钥"
    service="microsoft.compute"
    resource="virtualmachinescalesets"
    authors="gatneil"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>


# <a name="how-do-i-reset-the-password-or-ssh-key-on-my-scale-set-vms"></a>如何重置规模集 VM 上的密码或 SSH 密钥

若要重置用于对规模集 VM 进行身份验证的密码或 SSH 密钥，必须使用 VMAccessAgent 扩展（适用于基于 Windows 的规模集）或 VMAccessForLinux 扩展（适用于基于 Linux 的规模集）。

## <a name="recommended-documents"></a>建议的文档

有关详细信息，请参阅[此文档](https://azure.microsoft.com/blog/using-vmaccess-extension-to-reset-login-credentials-for-linux-vm/)，其中介绍了如何使用适用于基于 Linux 的规模集的 VMAccessForLinux 扩展。 对于基于 Windows 的规模集，请参考下面的示例 PowerShell 代码：

```powershell
$vmssName = "myvmss"
$vmssResourceGroup = "myvmssrg"
$publicConfig = @{"UserName" = "user"}
$privateConfig = @{"Password" = "********"}
 
$extName = "VMAccessAgent"
$publisher = "Microsoft.Compute"
$vmss = Get-AzureRmVmss -ResourceGroupName $vmssResourceGroup -VMScaleSetName $vmssName
$vmss = Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $extName -Publisher $publisher -Setting $publicConfig -ProtectedSetting $privateConfig -Type $extName -TypeHandlerVersion "2.0" -AutoUpgradeMinorVersion $true
Update-AzureRmVmss -ResourceGroupName $vmssResourceGroup -Name $vmssName -VirtualMachineScaleSet $vmss
```

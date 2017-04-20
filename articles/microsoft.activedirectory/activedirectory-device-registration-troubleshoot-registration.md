<properties
    pageTitle="Problems with device registrations and managing devices in Azure AD"
    description="Azure AD 中的设备注册和设备管理问题 "
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="spunukol"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="AzureADDeviceRegistration_Registration"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="problems-with-device-registrations-and-managing-devices-in-azure-ad"></a>Azure AD 中的设备注册和设备管理问题

## <a name="recommended-steps"></a>**建议的步骤**

1. 确保你有权在 Azure AD 和本地 AD 中执行操作。 只有 Azure AD 中的全局管理员可以管理设备注册设置。 此外，如果你要在本地 Active Directory 中设置自动注册，则你需是 Active Directory 和 AD FS（如果适用）的管理员。
    
2. 如果你要将设备直接注册到 Azure AD，同时要将其注册到 Intune，则首先需要确保已配置 Intune 并已获得许可。
    
3. 首次为本地 AD 设备设置自动设备注册时，请确保满足文档中列出的所有先决条件。
   
4.    提交票证之前，我们建议你查看此处所列的文档。 这些文档可帮助你设置 Azure AD 和设备注册以及进行故障排除。


## <a name="recommended-documents"></a>**建议的文档**
### <a name="setup-azure-ad"></a>设置 Azure AD ###

[设置加入 Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-overview) 

### <a name="setup-device-registration"></a>设置设备注册 ###

[为本地 Active Directory 设备设置自动注册] (https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-setup) 

### <a name="troubleshooting-common-issues-for-registration-and-managing-devices"></a>排查注册和设备管理的常见问题 ###

[排查 Windows 10 和 Windows Server 2016 注册问题](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows)  
[排查 Windows 7 和非 Windows 10/Windows Server 2016 注册问题](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows-legacy)  
[有关设备注册的常见问题解答](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-faq) 



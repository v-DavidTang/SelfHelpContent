<properties
    pageTitle="Problems with device registrations and managing devices in Azure AD"
    description="设备注册"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="spunukol"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32392474"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="problems-with-device-registrations-and-managing-devices-in-azure-ad"></a>Azure AD 中的设备注册和设备管理问题

## <a name="recommended-steps"></a>**建议的步骤**

1. 确保你有权在 Azure AD 和本地 AD 中执行操作。 只有 Azure AD 中的全局管理员可以管理设备注册设置。 此外，若要在本地 Active Directory 中设置自动注册，则你需是 Active Directory 和 AD FS（如果适用）的管理员。
2. 若要将设备直接注册到 Azure AD，同时要将其注册到 Intune，则首先需要确保[已配置 Intune](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune) 并已获得[许可](https://docs.microsoft.com/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune-step-3)。
3. 首次为本地 AD 设备设置自动设备注册时，请确保满足[文档中列出的所有先决条件](https://docs.microsoft.com/azure/active-directory/active-directory-device-registration-overview)。  


## <a name="recommended-documents"></a>**建议的文档**
### <a name="set-up-azure-ad"></a>设置 Azure AD ###

* [设置加入 Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-overview) 

### <a name="set-up-device-registration"></a>设置设备注册 ###

* [为本地 Active Directory 设备设置自动注册](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-setup) 

### <a name="troubleshooting-common-issues-for-registration-and-managing-devices"></a>排查注册和设备管理的常见问题 ###

* [排查 Windows 10 和 Windows Server 2016 注册问题](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows)

* [排查 Windows 7 和非 Windows 10/Windows Server 2016 注册问题](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows-legacy)

* [有关设备注册的常见问题解答](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-faq) 



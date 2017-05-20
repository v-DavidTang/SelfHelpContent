<properties
    pageTitle="Problems enrolling devices with Azure AD"
    description="将设备注册到 Azure AD 时遇到问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="problems-enrolling-devices-with-azure-ad"></a>将设备注册到 Azure AD 时遇到问题

**不知道如何将 Windows 7 电脑注册到 Azure AD**

也可以将已加入本地 Active Directory 域的 Windows 7 电脑注册到 Azure AD。 然后，可以在访问指定的云应用程序时，应用条件访问策略来要求使用已加入域的计算机。
<br><br>
有关详细信息，请参阅：
<br>
[如何为 Windows 7 设备设置条件性访问](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-setup)


**不知道如何增加用户可以注册的设备数**

在 Azure AD 门户中，可以设置用户可在 Azure AD 中使用的设备数上限。 如果用户达到此配额，则在删除一个或多个现有设备之前，他们无法添加其他设备。
<br><br>
有关详细信息，请参阅：
<br>
[如何设置用户可以注册的设备数](https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-setup)


**遇到了条件访问始终阻止设备的问题**

要求符合“设备已加入域”的策略失败的原因可能是设备未正确注册到 Azure AD。 必须将设备注册 Azure AD，以及用户进行身份验证和应用策略时能够提供有关设备的信息。 使用 PowerShell 读取 Azure AD 中的设备属性，即可验证设备信息。 
<br><br>
有关详细信息，请参阅：
<br>
[如何验证 Azure AD 中的设备信息](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-setup)

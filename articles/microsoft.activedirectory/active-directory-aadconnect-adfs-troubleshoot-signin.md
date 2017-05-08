<properties
    pageTitle="I have configured federation with Azure AD using AD FS but sign-in is failing"
    description="使用 Azure AD 联合登录失败"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="billmath"
    displayOrder="5"
    selfHelpType="generic"
    supportTopicIds="32570971"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="i-have-configured-federation-with-azure-ad-using-ad-fs-but-sign-in-is-failing"></a>我已使用 AD FS 配置了与 Azure AD 的联合，但登录失败

## <a name="recommended-steps"></a>**建议的步骤**

建议使用 Azure AD Connect 来配置与 Azure Active Directory 的联合。 Azure AD Connect 提供简单的步骤来配置和维护联合。 如果用户登录失败，请尝试以下常用解决方法，看看是否能起到作用 – 


1. [使用 AAD Connect 修复与 Azure AD 的信任关系](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#repairthetrust)
2. [使用多个域配置联合](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#addfeddomain)
3. [使用备用 ID 配置联合](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#federate-with-azure-ad-using-alternateid)
4. [为非 Internet Explorer 浏览器中的用户配置 WIA](https://technet.microsoft.com/windows-server-docs/identity/ad-fs/operations/configure-intranet-forms-based-authentication-for-devices-that-do-not-support-wia)


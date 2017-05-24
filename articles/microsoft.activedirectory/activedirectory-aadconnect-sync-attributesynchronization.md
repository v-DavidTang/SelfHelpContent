<properties
    pageTitle="Synchronizing AD to Azure AD/Synchronization problem for a specific attribute"
    description="将 AD 同步到 Azure AD/特定的属性出现同步问题"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32570976"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="synchronizing-ad-to-azure-adsynchronization-problem-for-a-specific-attribute"></a>将 AD 同步到 Azure AD/特定的属性出现同步问题

## <a name="recommended-steps"></a>建议的步骤

**如何选择要同步到 Azure AD 的特定属性**

  * 有关 Azure AD connect 同步的属性列表的信息，请参阅 [Azure AD Connect 同步：与 Azure Active Directory 同步的属性](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-attributes-synchronized)一文。

  * 如果想要限制同步到 Azure AD 的属性列表，请参阅文章部分 [Azure AD Connect 的自定义安装 - Azure AD 应用和属性筛选](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom#azure-ad-app-and-attribute-filtering)。

**某些属性不同步到 Azure AD 的问题**

考虑的要点：

  * 如果最近更新了要同步到 Azure AD 的属性列表，则必须记得先执行完全导入，然后执行增量同步。
  
  * 如果最近使用新的 AD 属性更新了本地 AD 架构并且想要将这些属性同步到 Azure AD，则必须先刷新 Azure AD Connect 中的架构，然后才可以包含这些属性进行目录同步。
  
  * 如果在将某些 User 对象的本地 Exchange AD 属性 (msExch-) 同步到 Azure AD 时出现问题，请务必检查是否填充了 User 对象中的 mailNickname 属性。 默认情况下，除非为 User 对象中的 mailNickname 属性赋了值，否则不会同步 Exchange AD 属性。

**LargeObject 错误**

  * 当某个属性超过 Azure Active Directory 架构设置的允许大小限制、长度限制或计数限制时，同步操作将导致 LargeObject 或 ExceededAllowedLength 同步错误。 通常，此错误发生在以下属性上：
    * userCertificate
    * userSMIMECertificate
    * thumbnailPhoto
    * proxyAddresses

  * 对于 userCertificate 和 userSMIMECertificate 属性，Azure AD 强制实施每个属性最多具有 15 个值的限制。 有关如何排查有关 userCertificate 的 LargeObject 错误的详细信息，请参阅[处理 userCertificate 属性导致的 LargeObject 错误](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-largeobjecterror-usercertificate)一文。

  * 对于 thumbnailPhoto 属性，Azure AD 强制实施 100KB 最大大小限制。

  * 对于 proxyAddresses，Azure AD 目前不会针对该属性本身强制实施硬限制。 但是，Azure AD 只允许对某个给定的 User 对象最多指定 1000 个属性值。 这包括所有属性，包括用户始终不可见的系统属性。
  


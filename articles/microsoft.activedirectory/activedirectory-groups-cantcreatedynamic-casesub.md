<properties 
    pageTitle="I can't create and populate a dynamic group"
    description= "创建和填充动态组时出现问题 "
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder=""
    supportTopicIds="32570978"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />



# <a name="i-cant-create-and-populate-a-dynamic-group"></a>无法创建和填充动态组

## <a name="recommended-steps"></a>**建议的步骤**
1.    如果找不到内置的用户属性，请确保该属性已列在 [支持的属性列表] (https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal#supported-properties) 中。
2.    如果要查找内置的设备属性，请确保该属性已列在[设备属性](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal#using-attributes-to-create-rules-for-device-objects)列表中。
3.    如果在“简单规则”下拉列表中找不到该属性，你也可以使用“高级规则”来构造高级规则的正文。 请确保语法正确，并且属性类型与值匹配。 另外，请确保在选择属性时已添加相应的对象前缀；例如，user.country、device.deviceOSType。
了解[有关如何创建高级规则的指导](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal#constructing-the-body-of-an-advanced-rule)。 
4.    除了内置的用户属性和设备属性以外，还可以使用[扩展属性](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal#extension-attributes-and-custom-attributes)。 创建简单规则时，这些属性应会显示在下拉列表中。 可以通过使用 PowerShell 查询用户的属性以及通过搜索属性名称，在目录中查找自定义属性名称。 构造高级规则时也可以使用这些方法。  
5.    确保租户具有相应的许可证。 动态组要求租户具有 Azure Active Directory P1 Premium 许可证。 可在[此处](https://www.microsoft.com/cloud-platform/azure-active-directory-pricing)访问 Azure Active Directory 许可计划列表。 可在[此处](https://www.microsoft.com/cloud-platform/enterprise-mobility-security-pricing)访问企业移动性 + 安全性许可计划。
6.    确保创建动态组的用户的角色是“公司管理员”或“用户管理员”。  
7.    请耐心等待在组中填充信息。 根据租户的大小，首次填充或者在更改规则后，最长可能需要 24 小时才能在组中完成填充。

## <a name="recommended-documents"></a>**建议的文档**

* [为动态组成员身份创建基于属性的规则](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) 


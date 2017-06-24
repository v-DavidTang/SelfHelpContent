<properties
    pageTitle="I still have other problems related to domain name management"
    description="Azure Active Directory 域疑难解答"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="4297"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain"
    productPesIds=""
    cloudEnvironments="public"
    />


# <a name="i-still-have-other-problems-related-to-domain-name-management"></a>仍然遇到与域名管理相关的其他问题
 
## <a name="recommended-steps"></a>**建议的步骤** 

1.    确保未在其他 Azure AD 租户或 Office 365 中配置你的域名。 如果已在 Office 365 中配置你的域名并尝试将该域名添加到其他 Azure AD 租户，则验证将会失败。 如果发生这种情况，请从已验证该域名的 Azure AD 租户中删除它，然后将它添加到你的 Azure AD 租户。 不能由两个不同的租户验证同一个自定义域名。
2.    如果组织中的某人已使用 PowerBI 或 Rights Management Services (RMS) 的自助注册，他们可能已创建非托管租户。 可以使用[管理员接管](https://docs.microsoft.com/azure/active-directory/active-directory-self-service-signup)功能来管理此租户，或者在 [PowerShell](https://docs.microsoft.com/powershell/msonline/v1/confirm-msoldomain) 中使用强制接管选项添加该域。
3.    如果尝试为联合单一登录配置自定义域名并且未设置 ADFS，则必须通过 Azure AD Connect 工具将目录中的联合设置配置为使用自定义域名。 
4.    如果尝试删除 Azure AD 租户，请确保与所要删除的租户关联的任何 Microsoft Online Services（例如 Microsoft Azure、Office 365 或 Azure AD Premium）不存在活动的订阅。 使用 [Azure 支持和计费](https://support.office.com/article/Contact-Office-365-for-business-support-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b)功能传输订阅或加急取消活动的订阅。

## <a name="recommended-documents"></a>**建议的文档**

* [添加自定义域名的子域](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#add-subdomains-of-a-custom-domain) 

* [Office 365 和 Azure AD 租户中的资源依赖关系](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-directory-independence) 

* [使用 PowerShell 或图形 API 管理域名](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#use-powershell-or-graph-api-to-manage-domain-names) 

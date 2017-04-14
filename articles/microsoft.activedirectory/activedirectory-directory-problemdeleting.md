 <properties
    pageTitle="Problem deleting an Azure AD tenant"
    description="Azure Active Directory 自助案例提交"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565595"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="problem-deleting-an-azure-ad-tenant"></a>删除 Azure AD 租户时出现问题 

## <a name="recommended-steps"></a>**建议的步骤**
1.    若要删除 Azure AD，你需是目录中的全局管理员。 请确保未使用登录帐户中包含类似于 contoso.onmicrosoft.com 的默认目录的帐户（例如 admin@contoso.onmicrosoft.com）登录。 
2.    如果该目录中包含任何活动的应用程序，必须先删除这些应用程序，然后才能删除 Azure AD。 导航到“应用注册”页并删除现有应用程序。 
3.    请确保与所要删除的目录关联的任何 Microsoft Online Services（例如 Microsoft Azure、Office 365 或 Azure AD Premium）不存在活动的订阅。 必须通过 Azure 支持和计费部门传输订阅或加急取消活动的订阅。 详细了解如何取消 Office 365 和 Azure 订阅。 
4.    尝试删除 Azure AD 时，请检查除你自己（全局管理员）以外，该目录中是否没有其他活动用户。 删除其他所有活动用户。另外，还需要删除租户中自定义域名的所有依赖项，例如，使用 admin@contoso.com 创建的用户。 

## <a name="recommended-documents"></a>**建议的文档**

* [Azure 订阅与 Azure AD 的关联方式](https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory) 
* [从 Azure Active Directory 中删除用户](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal)
* [删除目录中的应用程序](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#removing-an-application) 
* [将 Azure 订阅所有权转让给其他帐户](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
* [有关删除 Azure AD 的其他信息](https://docs.microsoft.com/azure/active-directory/active-directory-administer#how-can-i-delete-an-azure-ad-directory) 



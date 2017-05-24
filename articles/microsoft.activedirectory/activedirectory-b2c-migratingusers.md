 <properties
    pageTitle="Business to Consumer (B2C)/Creating or migrating users into B2C"
    description="企业对消费者 (B2C)/在 B2C 中创建用户或将用户迁移到其中"
    service="microsoft.azureactivedirectory"
    resource="b2cDirectories"
    authors="parakhj"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds="32416703"
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="how-to-create-or-migrate-users-into-azure-ad-b2c"></a>如何在 Azure AD B2C 中创建用户或将用户迁移到其中

创建可以通过 B2C 集成应用登录的 Azure AD B2C 用户的唯一方式是：

* 让用户通过[注册](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-policy)或[注册/登录](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-or-sign-in-policy)策略注册
* 使用[图形 API](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-graph-dotnet)

虽然可以通过 Azure 门户 UI 创建用户，但这些用户将无法登录并正常使用 Azure AD B2C。

如果希望能够通过该门户创建 Azure AD B2C 用户，可以在 [Azure AD B2C UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c) 论坛中请求此功能。

## <a name="recommended-documents"></a>**建议的文档**

* [Graph API](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-graph-dotnet)
* [堆栈溢出](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
* [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)

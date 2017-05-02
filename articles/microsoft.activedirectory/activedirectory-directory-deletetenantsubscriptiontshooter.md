<properties 
    pageTitle="I have Microsoft Online Services blocking deletion of my Azure AD"
    description="Microsoft Online Services 阻止删除 Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1870"
    supportTopicIds="32565594"
    selfHelpType="resource"
    resourceTags="directory_delete"
    productPesIds="14785" 
    cloudEnvironments="public"
 />


# <a name="i-have-microsoft-online-services-blocking-deletion-of-my-azure-ad"></a>Microsoft Online Services 阻止删除 Azure AD

## <a name="recommended-steps"></a>**建议的步骤**

组织的订阅与需要用户级许可证分配的产品（例如 Office 365 企业版 E3、企业移动性 + 安全性或 Azure AD Premium）相关。 若要删除某个 Azure AD 租户，与该租户关联的所有订阅都需要处于完全“已取消预配”状态。 发生以下一个或多个活动后，将发生取消预配：

* 管理中心内已取消的订阅在取消至少 180 天后被删除，并标记为“已取消预配”
* 将订阅传输到另一个租户
* 创建支持请求，要求立即取消订阅。 详细了解[订阅生命周期管理和保留](https://support.office.com/article/What-happens-to-my-data-and-access-when-my-Office-365-for-business-subscription-ends-4436582f-211a-45ec-b72e-33647f97d8a3)。

若要查看租户中所有订阅的列表，请转到[“Office 365 管理中心”-&gt;“计费”-&gt;“订阅”](https://portal.office.com/adminportal/home#/subscriptions)。 可查看每种类型的订阅产品（例如试用版或付费版）及其状态（活动或即将过期）。

管理订阅的方式取决于订阅最初的购买方式：

1.  基于客户的付费版或试用版订阅（如 Office 365 企业版 E3、EMS 或 Azure AD Premium）可以通过 Office 365 管理门户进行管理。 如果你想要取消某个订阅，可执行以下步骤：导航到管理门户，转到“订阅”页，在列表中找到想要管理的订阅，选择“取消”。 然后选择“确认取消”。 如果你希望在订阅的自然生命周期结束*之前*尽快取消该订阅，以便能够删除 Azure AD 租户，则需要通过支持部门提升该事务的优先级。 详细了解 [Azure 计费或 Office 365 商业版支持](https://support.office.com/article/Contact-Office-365-for-business-support-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b)。

2.  根据企业协议 (EA) 购买的订阅无法在管理中心取消。 请在帐户经理的帮助下管理 EA 订阅。 详细了解[企业协议注册](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer#can-i-migrate-from-pay-as-you-go-to-cloud-solution-provider)

3.  云解决方案提供商 (CSP) 合作伙伴创建的订阅无法在管理中心取消。 请使用管理中心提供的与该订阅相关的信息联系该合作伙伴。

如果想要将 Azure 订阅转移到不同的 Azure AD 租户或 Office 365，可在帐户中心通过自助传输移动即用即付、Visual Studio、Action Pack 或 BizSpark 订阅。 详细了解如何[转让 Azure 订阅的所有权](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)。

## <a name="recommended-documents"></a>**建议的文档**

* [Azure 订阅与 Azure AD 的关联方式](https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory) 
* [从 Azure Active Directory 中删除用户](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal)
* [删除目录中的应用程序](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#removing-an-application) 
* [将 Azure 订阅所有权转让给其他帐户](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
* [有关删除 Azure AD 的其他信息](https://docs.microsoft.com/azure/active-directory/active-directory-administer#how-can-i-delete-an-azure-ad-directory) 

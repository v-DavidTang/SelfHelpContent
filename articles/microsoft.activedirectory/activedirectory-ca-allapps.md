<properties
    pageTitle="Problems setting policy that applies to 'all cloud apps'"
    description="设置应用到“所有云应用”的策略时遇到问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="problems-setting-policy-that-applies-to-all-cloud-apps"></a>设置应用到“所有云应用”的策略时遇到问题

将对任何网站或 Web 服务强制实施应用到“所有云应用”的条件访问策略。 这包括 Azure 门户。 由于该策略会产生广泛的影响，因此我们建议先对少量的用户实施并验证该策略，然后再对所有用户实施。

## <a name="recommended-steps"></a>**建议的步骤**

*    当策略将应用于所有云时，请确保排除管理员帐户
*    在应用于管理员帐户之前确保策略按预期发挥作用

有关详细信息，请参阅：
<br>
[设置条件访问时如何避免帐户锁定](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal#what-you-should-avoid-doing)

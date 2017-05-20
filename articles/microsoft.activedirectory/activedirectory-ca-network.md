<properties
    pageTitle="Problems configuring location-based conditional access"
    description="配置基于位置的条件访问时遇到问题"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="problems-configuring-location-based-conditional-access"></a>配置基于位置的条件访问时遇到问题

可将条件访问策略绑定到用于连接 Azure Active Directory 的客户端的位置。 可使用以下选项： <br>

*    在 Azure AD 中为公司配置[受信任的 IP 范围](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next#trusted-ips) <br>
*    使用 ADFS [企业网络内部声明](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-cloud)来指明用户位于企业网络中。

使用条件访问策略的位置条件可将策略应用到不在受信任网络中的位置。 为此，可以设置包含“所有位置”（表示来自任何位置）的策略条件，并排除“所有受信任的 IP”。 
<br><br>
有关详细信息，请参阅：
<br>
[如何为条件访问配置“工作”网络](http://aka.ms/calocation) <br>
[如何在 Azure AD 中配置受信任的 IP 范围](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next#trusted-ips) <br>
[如何配置 ADFS 企业网络内部声明](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-cloud)

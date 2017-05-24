<properties
    pageTitle="Virtual Network selection and configuration issues"
    description="Azure AD 域服务"
    service="microsoft.aad"
    resource="Microsoft_AAD_DomainServices"
    authors="arluca"
    selfHelpType="generic"
    supportTopicIds="32570966"
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="virtual-network-selection-and-configuration-issue"></a>虚拟网络选择和配置问题

## <a name="recommended-steps"></a>**建议的步骤**
1.    如果打算使用现有的虚拟网络，请确保该网络部署在 Azure AD 域服务托管域所在的同一 [Azure 区域](https://azure.microsoft.com/regions/#services/)。 
2.  如果打算使用现有的虚拟网络，确保它是经典 Azure [区域虚拟网络](https://docs.microsoft.com/azure/virtual-network/virtual-networks-migrate-to-regional-vnet)。 注意：在使用 Azure Resource Manager 创建的虚拟网络中无法启用 Azure AD 域服务。
3.  如果打算使用现有的虚拟网络，请确保 
4.  确保该虚拟网络中未配置自定义 DNS 服务器。 
5.  确保现有域的名称与该虚拟网络中使用的域名不同。
6.  如果需要将 Azure AD 域服务经典虚拟网络连接到基于 Resource Manager 的虚拟网络，请参阅[网络连接](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-networking#network-connectivity)。

## <a name="recommended-documents"></a>**建议的文档**
* [将传统虚拟网络迁移到区域虚拟网络](https://docs.microsoft.com/azure/virtual-network/virtual-networks-migrate-to-regional-vnet)
* [Azure AD 域服务故障排除指南](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting) 
* [Azure AD 域服务常见问题解答](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)


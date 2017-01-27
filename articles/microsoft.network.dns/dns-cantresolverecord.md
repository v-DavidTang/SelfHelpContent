<properties 
    pageTitle="I can't resolve my DNS record"
    description="无法在 Azure DNS 托管的 DNS 区域解析新 DNS 记录。"
    service="microsoft.network"
    resource="dnszones"
    authors="jtuliani"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>


# <a name="i-cant-resolve-my-dns-record"></a>无法解析 DNS 记录

## <a name="recommended-steps"></a>**建议的步骤**

DNS 名称解析是一个多步骤过程，该过程失败存在多种原因。 以下步骤有助于调查为何无法在 Azure DNS 托管的区域对 DNS 记录进行 DNS 解析。

1.  确保已在 Azure DNS 中正确配置 DNS 记录。 在 Azure 门户中查看 DNS 记录，检查区域名称、记录名称和记录类型是否正确。
2.  确保可在 Azure DNS 名称服务器上正确解析 DNS 记录。
    - 如果从本地电脑查询 DNS，可能会发现缓存结果未反映名称服务器当前的状态。  此外，企业网络通常使用 DNS 代理服务器，这些服务器会阻止 DNS 查询定向到特定名称服务器。  若要避免这些问题，请使用基于 Web 的名称解析服务，例如 [digwebinterface](http://digwebinterface.com)。
    - 请务必为 DNS 区域指定正确的名称服务器，如 Azure 门户中所示。
    - 检查 DNS 名称是否正确（必须指定完全限定的名称，包括区域名称），以及记录类型是否正确
3.  确保 DNS 域名已正确[委托给 Azure DNS 名称服务器](https://docs.microsoft.com/azure/dns/dns-domain-delegation)。 存在[许多提供 DNS 委托验证的第三方网站]( https://www.bing.com/search?q=dns+check+tool)。 这是*区域*委派测试，因此应只输入 DNS 区域名称，而不是完全限定的记录名称。
4.  完成上述步骤后，现在应可以正确解析 DNS 记录。 若要进行验证，可再次使用 [digwebinterface](http://digwebinterface.com)，这次请使用默认名称服务器设置。

如果上述步骤未解决该问题，请将此问题发布到 [MSDN 上的社区支持论坛](https://social.msdn.microsoft.com/Forums/en-US/home?forum=WAVirtualMachinesVirtualNetwork)或创建 Azure 支持请求。

## <a name="recommended-documents"></a>**建议的文档**

[将域委托给 Azure DNS](https://docs.microsoft.com/azure/dns/dns-domain-delegation)





<!--HONumber=Jan17_HO4-->



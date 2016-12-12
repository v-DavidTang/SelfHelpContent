<properties
    pageTitle="The response on endpoints is slow or varies a lot"
    description="终结点上的响应速度缓慢或变化很大"
    service="microsoft.network"
    resource="trafficmanagerprofiles"
    authors="radwiv"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="the-response-on-endpoints-is-slow-or-varies-a-lot"></a>终结点上的响应速度缓慢或变化很大

流量管理器在 DNS 层为给定请求选择最佳终结点。 基于所选路由类型选择终结点。
选择终结点后，客户端直接连接到该终结点，且流量管理器不会介入该流。

## <a name="recommended-steps"></a>**建议的步骤**

1. 如果终结点是 Azure 资源，则在浏览器中测试探测路径，并检查是否会有所改善。
2. 如果性能仍旧较慢，请在指向流量管理器的域名上运行 nslookup。 这将提供 DNS 服务器的位置。
3. 请参阅 Azure 门户中该服务的“诊断和解决问题”部分。


## <a name="recommended-documents"></a>**建议的文档**
[Windows Azure Traffic Manager Performance Impact](https://blogs.msdn.microsoft.com/kwill/2013/09/17/windows-azure-traffic-manager-performance-impact)（Microsoft Azure 流量管理器性能影响）



<!--HONumber=Dec16_HO1-->



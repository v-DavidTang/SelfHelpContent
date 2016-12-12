<properties
    pageTitle="Traffic Manager is directing requests to disabled endpoint"
    description="流量管理器将请求定向到已禁用的终结点"
    service="microsoft.network"
    resource="trafficmanagerprofiles"
    authors="radwiv"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="traffic-manager-is-directing-requests-to-disabled-endpoint"></a>流量管理器将请求定向到已禁用的终结点

## <a name="recommended-steps"></a>**建议的步骤**

1. 缓存的响应可能是导致将请求定向到已禁用的终结点的原因。 将生存时间 (TTL) 设置为较低的值可能会解决此问题。 较低的 TTL 会使得缓存的条目更快过期，但这可能会导致流量管理器服务收到更多请求。<br>
   默认 TTL 值为 300 秒，最小可设置为 30 秒。


## <a name="recommended-documents"></a>**建议的文档**

[流量管理器终结点](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-endpoint-types)<br>
[流量管理器终结点监视和故障转移](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-monitoring)



<!--HONumber=Dec16_HO1-->



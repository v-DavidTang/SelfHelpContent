<properties
    pageTitle="Microsoft Graph service performance"
    description="Microsoft Graph 服务性能"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="PatAltimore"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32134062"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
/>


# <a name="microsoft-graph-service-performance"></a>Microsoft Graph 服务性能

## <a name="my-application-is-being-throttled"></a>应用程序被限制

限制可在限定针对服务发出的并发调用数，以防止过度使用资源。 Microsoft Graph 能够处理极大量的请求。 在请求数过多的情况下，限制可帮助保持 Microsoft Graph 服务的最佳性能和可靠性。 

Microsoft Graph<br>
考虑[使用增量查询来跟踪 Microsoft Graph 数据的更改](https://developer.microsoft.com/graph/docs/concepts/delta_query_overview)，以减少应用发出的请求总数。 如果减少请求总数，应用就不太可能会受到限制的影响。

Azure Active Directory Graph<br>
[Azure AD 限制指南](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-throttling)<br>
[批处理](https://msdn.microsoft.com/Library/Azure/Ad/Graph/howto/azure-ad-graph-api-batch-processing)是可以减少请求总数的选项。 如果减少请求总数，应用就不太可能会受到限制的影响。

## <a name="where-can-i-find-details-about-the-graph-api-throttle-limits"></a>在哪里可以找到有关图形 API 限制的详细信息？

限制行为可能与请求的类型和数目相关。 例如，如果请求数量极大，则所有请求类型都会受到限制。 阈值限制根据请求类型的不同而异。 因此，你可能会遇到写入被限制，但读取仍受允许的情况。 由于许多因素会影响限制行为，因此我们不会发布特定的限制。 

Microsoft Graph<br>
[Microsoft Graph 错误响应和资源类型](https://developer.microsoft.com/graph/docs/overview/errors)

Azure Active Directory Graph<br>
[Azure AD Graph 限制指南](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-throttling)

<properties 
    pageTitle="Why can't I view my namespace in the portal?" 
    description="为何在门户中看不到我的命名空间？" 
    service="microsoft.relay"
    resource="namespaces"
    authors="jtaubensee"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="" 
    productPesIds="16123"
    cloudEnvironments="public" 
/>


# <a name="i-cant-view-my-namespace-here-in-the-portal-but-i-can-see-it-in-the-classic-portal"></a>在新门户中看不到我的命名空间，但在经典门户中可以看到

## <a name="recommended-steps"></a>**建议的步骤**
* 我们最近对命名空间做了区分，其类型专门一与我们的服务相关。 也就是说，如果在经典门户中创建了“消息传送”或“事件中心”类型的命名空间，但在该命名空间中包含了中继实体，那么，该命名空间不会在新门户中显示。 若要在新门户中查看中继，这些中继的命名空间类型需是“中继”。 有关详细信息，请阅读这篇[博客](https://blogs.msdn.microsoft.com/servicebus/2016/09/14/azure-service-bus-messaging-relay-and-event-hubs-namespace-separation/)。 强烈建议在使用 ARM 为中继创建任何新命名空间时采用“中继”类型，或者在新门户中创建中继，因为自动创建的中继就是采用这种类型。

## <a name="recommended-documents"></a>**建议的文档**
[常见问题](https://azure.microsoft.com/documentation/articles/relay-faq)<br>
[常见的中继异常](https://azure.microsoft.com/documentation/articles/relay-exceptions)


<!--HONumber=Nov16_HO1-->



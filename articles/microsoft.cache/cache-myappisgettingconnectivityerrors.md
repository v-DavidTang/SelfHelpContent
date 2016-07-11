<properties
    pageTitle="My app is getting connectivity errors"
    description="我的应用出现连接错误"
    service="microsoft.cache"
    resource="redis"
    authors="kasparks"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 我的应用出现连接错误

## **建议的步骤**
若要解决最常见问题，请尝试下面的一种或多种方法。

1. 为平台使用推荐的客户端配置。<br>
[按语言列出的推荐 Redis 客户端](http://redis.io/clients)
2. 检查是否超出了客户端连接数上限。<br>
[了解客户端连接数限制](http://aka.ms/redistroubleshoortfaq)
3. 如果托管在 Azure 虚拟网络 (VNet) 上，请检查端口是否未被阻止。<br>
[Redis 缓存和 VNet 的常见错误配置问题](http://aka.ms/redistroubleshootvnet)
4. 你是否扩展了客户端应用？ 扩展时，可能会暂时断开连接。 完成扩展操作后，客户端应会重新连接。

## **建议的文档**
[我应使用哪种 Redis 缓存产品和大小？](http://aka.ms/redistroubleshootoffering)



<!--HONumber=Jun16_HO5-->



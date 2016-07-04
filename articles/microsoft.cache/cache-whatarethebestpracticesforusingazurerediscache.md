<properties
    pageTitle="What are the best practices for using Azure Redis Cache?"
    description="Azure Redis 缓存的最佳用法是怎样的？"
    service="microsoft.cache"
    resource="redis"
    authors="kasparks"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# Azure Redis 缓存的最佳用法是怎样的？

## **建议的步骤**
若要详细了解最佳实践，请尝试以下一项或多项操作。

1. 为应用程序使用最新版本的客户端库。<br>
[按语言列出的 Redis 客户端](http://redis.io/clients)
2. 基本层仅用于开发/测试，不附带 SLA。 标准或高级层建议用于生产用途。
3. 使用 Redis 数据持久性来提高复原能力，以防数据丢失。<br>
[详细了解如何配置 Redis 数据持久性](https://azure.microsoft.com/documentation/articles/cache-how-to-premium-persistence/)
4. 使用以下文章详细了解有关提高缓存性能和可缩放性的最佳实践。<br>
[详细了解最佳实践](http://aka.ms/redistroubleshootpnp)

## **建议的文档**
[我应使用哪种 Redis 缓存产品和大小？](http://aka.ms/redistroubleshootoffering)



<!--HONumber=Jun16_HO3-->



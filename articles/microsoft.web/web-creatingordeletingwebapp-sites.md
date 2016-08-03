<properties
    pageTitle="配置和管理/创建或删除 Web 应用"
    description="配置和管理/创建或删除 Web 应用"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32542209"
    resourceTags=""
    productPesIds="14748"
    cloudEnvironments="public"
/>


# 配置和管理/创建或删除 Web 应用

## **建议的步骤**
如果你无法删除 App Service 计划，请检查是否有任何资源与你尝试删除的 App Service 计划相关联。  从计划中删除所有关联的实体，你应该可以删除该计划。 另一个常见问题是在尝试使用以前已删除的名称创建网站时遇到“预配失败”错误。 请遵循以下步骤来解决该问题：

1. 使用你最初创建网站时所用的订阅 ID 连接到新门户 (portal.azure.com)。
2. 创建一个网站，其名称与你尝试创建的网站完全相同。 这样就会将新网站连接到以前删除的站点。
3. 转到旧门户 (manage.windowsazure.com) 并删除该站点。 这会删除以前网站中留下的所有内容。
4. 在旧门户中重新创建该网站。

## **建议的文档**
[此处介绍了每个 App Service 计划的限制](https://azure.microsoft.com/pricing/details/app-service/plans/)



<!--HONumber=Jul16_HO4-->



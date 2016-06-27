<properties
    pageTitle="发出 API 请求后，我收到 401 错误"
    description="发出 API 请求后，我收到 401 错误"
    service="microsoft.cognitiveservices"
    resource="accounts"
    authors="kasparks"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 发出 API 请求后，我收到 401 错误

## **建议的步骤**
若要解决大多数常见问题，请尝试下面的一个或多个步骤。

1. 可能未在标头或查询字符串中正确发送所用的 API 密钥。 例如，在发送 HTTP POST 请求时，请将密钥放入“Ocp-Apim-Subscription-Key”标头，或放入查询字符串中的“Subscription-Key={key}”。
2. 检查 Azure 订阅状态以确保其处于活动状态。<br>
单击“订阅”打开“订阅”边栏选项卡，然后检查状态。
3. 查看具体 API 的文档，以找到有关特定错误代码的详细信息。

## **建议的文档**
[认知服务文档](https://www.microsoft.com/cognitive-services/en-us/documentation)



<!--HONumber=Jun16_HO3-->



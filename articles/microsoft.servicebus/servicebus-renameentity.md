<properties 
    pageTitle="How can I rename a queue/topic after I create it?" 
    description="创建队列/主题后如何将它重命名？" 
    service="microsoft.servicebus"
    resource="namespaces"
    authors="jtaubensee"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="" 
    productPesIds="13186"
    cloudEnvironments="public,BlackForest,Fairfax" 
/>


# <a name="how-can-i-rename-a-queuetopic-after-i-create-it"></a>创建队列/主题后如何将它重命名？

## <a name="recommended-steps"></a>**建议的步骤**
* 无法在门户中更改队列名称，但是，你可以使用 NamespaceManager API 和 RenameQueue 方法来实现此目的。 请注意，这只适用于采用基本和标准消息传送计划的客户。

## <a name="recommended-documents"></a>**建议的文档**
[有关 NamespaceManager 类和管理实体的详细信息](https://msdn.microsoft.com/library/azure/microsoft.servicebus.namespacemanager.aspx)


<!--HONumber=Nov16_HO5-->



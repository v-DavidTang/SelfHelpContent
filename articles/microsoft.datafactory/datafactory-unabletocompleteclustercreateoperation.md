<properties 
    pageTitle="Unable to complete the cluster create operation" 
    description="预配按需 HDInsight 群集时出错：无法完成群集创建操作。 错误代码：400" 
    service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="6"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>


# 无法完成群集创建操作并返回错误代码 400
当预配按需 HDInsight 群集失败时，你可能会看到此错误。 

## **建议的步骤**
在使用 **HDInsightOnDemand** 类型的链接服务时，需要指定指向 Azure Blob 存储的 linkedServiceName。 数据工厂服务使用此存储来存储按需 HDInsight 群集的日志和支持文件。  有时，预配按需 HDInsight 群集会失败并出现以下错误：

“未能创建群集。 异常: 无法完成群集创建操作。 操作失败，代码为 '400'。 群集保持为 'Error' 状态。 消息: 'StorageAccountNotColocated'。”

此错误通常表示 linkedServiceName 中指定的存储帐户的位置，不是预配 HDInsight 时所在的同一个数据中心位置。 例如，如果 Azure 数据工厂的位置在美国西部，按需 HDInsight 预配在美国西部发生，但 Azure Blob 存储帐户位置设置为美国东部，那么，按需预配将会失败。

此外，在另一个 JSON 属性 additionalLinkedServiceNames 中，可能指定了按需 HDInsight 中的其他存储帐户。 其他这些链接存储帐户应该与 HDInsight 群集位于同一个位置，否则操作将会失败并出现相同的错误。

## **建议的文档**
[HDInsight 按需链接服务](https://azure.microsoft.com/documentation/articles/data-factory-compute-linked-services/#azure-hdinsight-on-demand-linked-service)


<!--HONumber=Jul16_HO1-->



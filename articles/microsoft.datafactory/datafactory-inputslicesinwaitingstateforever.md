<properties 
    pageTitle="Input slices are in Waiting state for ever" 
    description="输入切片始终处于 waiting 状态。" 
    service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="2"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>


# 输入切片始终处于 Waiting 状态

## **建议的步骤**
切片可能会出于许多原因而处于 **Waiting** 状态，其中一个常见原因是 **external** 属性未设置为 **true**。 在 Azure 数据工厂范围外部生成的任何数据集都应标记为 **external** 属性。 这表示该数据是外部的，而不是由数据工厂内的任何管道提供支持。 当数据出现在相应的存储中后，数据切片将标记为 **Ready**。 

有关 **external** 属性的用法，请参阅以下示例。 将 external 设置为 true 时，可以选择指定 **externalData***。 

有关此属性的详细信息，请参阅[数据集](https://azure.microsoft.com/en-us/documentation/articles/data-factory-create-datasets/)。
    
    {
      "name": "CustomerTable",
      "properties": {
        "type": "AzureBlob",
        "linkedServiceName": "MyLinkedService",
        "typeProperties": {
          "folderPath": "MyContainer/MySubFolder/",
          "format": {
            "type": "TextFormat",
            "columnDelimiter": ",",
            "rowDelimiter": ";"
          }
        },
        "external": true,
        "availability": {
          "frequency": "Hour",
          "interval": 1
        },
        "policy": {
          }
        }
      }
    }

若要解决该错误，请将 **external** 属性和可选的 **externalData** 节添加到输入表中的 JSON 定义中，然后重新创建表。 

## **建议的文档**
- [监视和管理 Azure 数据工厂管道](https://azure.microsoft.com/documentation/articles/data-factory-monitor-manage-pipelines/)
- [计划和执行](https://azure.microsoft.com/documentation/articles/data-factory-scheduling-and-execution/)



<!--HONumber=Jul16_HO1-->



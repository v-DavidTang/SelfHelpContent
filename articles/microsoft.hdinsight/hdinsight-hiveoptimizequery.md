<properties
    pageTitle="My hive queries are really slow"
    description="Hive 查询速度真的很慢"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds="32511190"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>


# <a name="my-hive-queries-are-really-slow"></a>Hive 查询速度真的很慢

## <a name="recommended-steps"></a>**建议的步骤**
可向群集应用以下 Hive 性能优化方法：
 
 1. 扩展工作节点，以利用更多可并行运行的映射器和化简器。
 2. 启用 Tex（而不是 MapReduce）作为执行引擎。
 3. 检查分区方案，考虑分区过多或过少的情况。 选择可让分区大小保持均等的方案。
 4. 使用 ORCFile 格式（已针对提高数据访问速度进行优化）。
 5. 启用矢量化来统一处理多行。

## <a name="recommended-documents"></a>**建议的文档**
[优化 Hive 性能](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-optimize-hive-query)<br>


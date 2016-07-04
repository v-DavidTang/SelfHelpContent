<properties
    pageTitle="I can't add nodes to my cluster"
    description="无法将节点添加到我的群集"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="matt1883"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 无法将节点添加到我的群集

## **建议的步骤**
 若要解决常见问题，请尝试下面的一个或多个步骤。
 
 1. [检查以确定群集位置是否有任何核心可用](data-blade:Microsoft_Azure_HDInsight.CoresUsageBreakdownBlade)。
 2. 使用[缩放群集功能](data-blade:Microsoft_Azure_HDInsight.ScaleClusterBlade)计算群集所需的附加核心数。 此值基于新辅助角色节点中的核心总数。
 3. 查看其他位置可用的核心数。 考虑在具有足够可用核心的其他位置重新创建群集。
 4. 如果想要提高特定位置的核心配额，请开具一份支持票证，指出你想要提高 HDInsight 核心配额。

## **建议的文档**
[在门户中管理群集 - 缩放群集](https://azure.microsoft.com/documentation/articles/hdinsight-administer-use-portal-linux/#scale-clusters)<br>



<!--HONumber=Jun16_HO5-->



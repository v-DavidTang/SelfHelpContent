<properties
    pageTitle="Spark application failed with OutOfMemoryError"
    description="Spark 应用程序失败并出现 OutOfMemoryError"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds="32511213"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>


# Spark 应用程序失败并出现 OutOfMemoryError
<a id="spark-application-failed-with-outofmemoryerror" class="xliff"></a>

此异常的最可能原因是未将足够的堆内存分配给作为执行程序或驱动程序（属于 Spark 应用程序）启动的 Java 虚拟机 (JVM)。

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>
1. 确定 Spark 应用程序将要处理的数据大小上限。 可以根据输入数据的最大大小、转换输入数据时生成的中间数据，以及进一步转换中间数据时生成的输出数据来做出推测。 如果无法做出正式的初始推测，此过程也可能是迭代性的。
2. 请确保要使用的 HDInsight 群集具有足够的内存和核心资源，以便能够适应 Spark 应用程序。 若要确定资源是否足够，可以在群集的 YARN UI 的“群集指标”部分中查看“已用内存与内存总计”以及“已用 VCore 与 VCore 总计”的值。
3. 将 Spark 配置设置为不超过 YARN 中显示的可用内存和核心数的 90%、但仍在 Spark 应用程序内存要求范围内的适当值。

## **建议的文档**
<a id="recommended-documents" class="xliff"></a>
[Spark 应用程序失败并出现 OutOfMemoryError](https://hdinsight.github.io/spark/spark-application-failure-with-outofmemoryerror.html)<br>


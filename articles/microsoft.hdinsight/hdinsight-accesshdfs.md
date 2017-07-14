<properties
    pageTitle="Access HDFS from the cluster"
    description="从群集访问 HDFS"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathb"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>


# 从群集访问 HDFS
<a id="access-hdfs-from-the-cluster" class="xliff"></a>

## **建议的步骤**
<a id="recommended-steps" class="xliff"></a>
若要从 HDInsight 群集内部访问本地 HDFS 而不是 WASB 或从 ADLS，请使用以下两个步骤之一。

1. 从命令行：使用命令 - `hdfs dfs -D "fs.default.name=hdfs://mycluster/" <commandName>`
2. 从应用程序：从应用程序访问文件系统时，请用作 HDFS URI“hdfs://mycluster/”


<properties 
    pageTitle="作业消耗了过多的流式处理单位"
    description="作业消耗了过多的流式处理单位"
    service="microsoft.streamanalytics"
    resource="streamingjobs"
    authors="samacha"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="my-job-consumes-too-many-streaming-units"></a>作业消耗了过多的流式处理单位

## <a name="recommended-steps"></a>**建议的步骤**
流式处理单位 (SU) 代表执行 Azure 流分析作业所消耗的计算资源。 在已经对 CPU、内存以及读取和写入速率进行测量的情况下，可以使用 SU 来描述相对的事件处理能力。

选择特定作业所需的 SU 数目时，得根据输入的分区配置以及为作业定义的查询来决定。 在“缩放”边栏选项卡中可以设置正确的所需缩放单位数。  

分配的流式处理单位数最好是超过所需的数目。 ASA 处理引擎会针对延迟和吞吐量进行优化，不过，代价是占用的内存会增加。 [有关可缩放性以及为作业配置缩放的详细信息](https://azure.microsoft.com/documentation/articles/stream-analytics-scale-jobs/) 

一般而言，对于未 PARTITION BY 的查询，一开始最好使用 6 个流式处理单位，在可以正常处理有代表性的数据量之后，使用试错方法，通过适当修改流式处理单位的数量并检查 SU %Utilization 指标，来确定最合理的流式处理单位数量。 

在开始进行任何处理之前，Azure 流分析将事件保留在一个名为“重新排序缓冲区”的窗口中。 事件在重新排序窗口内部按时间排序，后续操作将会针对临时排序的事件执行。 按时间对事件重新排序可确保运算符能够看到规定时间范围内的所有事件，从而能够执行必要的处理和生成输出。 此机制的一个副作用是，处理会出现延迟，延迟的时间长短即是重新排序窗口的持续时间。 作业的内存占用量（影响流式处理单位的消耗）取决于此重新排序窗口的大小及其包含的事件数。 

内存利用率偏高、使得作业使用的流式处理单位较多的最常见原因包括 

_1) GROUP BY 的基数较高_

传入事件的基数指示作业的内存使用量。 

例如，在 `Select count(*) from input group by clustered, tumblingwindow (minutes, 5)` 中，与 clustered 关联的数字就是查询的基数。 

为了消除基数较高造成的问题，可以通过使用 Partition By 增加分区来扩展查询，如下所示： 

~~~~
Select count(*) from input 
partition by clusterid 
group by clustered tumblingwindow (minutes, 5)
~~~~

`clustered` 的数目 

将查询分区后，它将会分散到多个节点中。 因此，可以通过降低重新排序缓冲区的大小来减少传入每个节点的事件数。  

Eventhub 分区应按 partitionid 进行分区。

_2) Join 的不匹配事件数较大_

联接中的不匹配事件数会影响查询的内存利用率。 以下查询将查找产生点击量的广告印象： 

~~~~
SELECT id from clicks INNER JOIN,
impressions on impressions.id = clicks.id AND datediff(hour, impressions, clicks) between 0 AND 10
~~~~

有可能显示了很多广告，但很少有人点击它们，并且需要保留该时间范围内的所有事件。 内存消耗量与时间范围大小和事件发生速率成比例。 

为了解决此问题，可以通过使用 partition by 增加分区来扩展查询。 

将查询分区后，它将会分散到多个节点中。 因此，可以通过降低重新排序缓冲区的大小来减少传入每个节点的事件数。  

_3) 存在大量的失序事件_ 

如果在一个较大的时间范围内出现大量的失序事件，将会导致“重新排序缓冲区”变大。 为了解决此问题，可以通过使用 partition by 增加分区来扩展查询。 将查询分区后，它将会分散到多个节点中。 因此，可以通过降低重新排序缓冲区的大小来减少传入每个节点的事件数。  

_建立 Microsoft 支持案例_ 

如果仍然无法判断出问题所在，请转到操作日志，选择一个最新的条目，单击“详细信息”按钮，然后复制该页面上的所有详细信息并将其提供给 Microsoft 支持部门。 

此外，如果可能，请包含示例数据，描述作业应该在相应的时间生成输出。  



<!--HONumber=Dec16_HO3-->



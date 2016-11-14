<properties 
    pageTitle="My job is not seeing any inputs"
    description="在作业中看不到任何输入"
    service="microsoft.streamanalytics"
    resource="streamingjobs"
    authors="kschaefer13"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="my-job-is-not-seeing-any-inputs"></a>在作业中看不到任何输入

## <a name="recommended-steps"></a>**建议的步骤**
1. 使用每项输入对应的“测试连接”按钮来验证与输入和输出的连接。 如果验证失败，请验证输入的源或输出接收器的凭据。 
2. 使用“服务总线资源管理器”连接到 Azure EventHub（如果使用了 EventHub 输入），验证输入数据是否流入 EventHub。 
3. 使用每项输入对应的“示例数据”按钮下载输入示例数据。 
    * 验证 CSV 是否包含每个事件或事件批的标头。 
    * 如果输出是 SQL，请验证 CSV 标头是否不包含空格。 
4. 检查示例数据，了解数据的形式：架构和数据类型。 
5. 在“查询”选项卡中，使用“测试”按钮测试查询，并使用下载的示例数据测试查询。 检查并尝试修正所有错误。  
6. 键入查询，启动作业，然后使用较小的负载检查作业是否按预期运行。 
7. 一旦作业状态更改为“正在运行”，经过查询中指定的持续时间后，可以在接收器数据源中看到输出。 
8. 如果在经过预期的持续时间（基于查询）之后未获得任何输出，请尝试以下操作： 
    * 在“监视器”选项卡上查看“监视指标”。 此处的指标会延迟大约几分钟显示，因为它们是过去一分钟的聚合值。 
    * 查看“输入事件数”、“运行时错误数”和“数据转换错误数”的指标。 
        * 如果“输入事件数”大于 0，则 ASA 作业可以读取数据。 否则，可能表示存在问题 
            * 如果使用了 Timestamp By，请确保事件中的时间戳大于开始时间。 
            * 使用服务总线资源管理器（如果将事件中心用作输入）查看数据源，确定它是否包含此作业的有效数据 
            * 检查数据序列化格式和编码是否符合预期。 
            * 如果使用事件中心，消息正文可能为 Null。 

如果没有问题，则需要分析数据流。 可以在流分析作业的“设置”边栏选项卡中单击“作业关系图”按钮，使用能够直观显示作业的作业关系图对数据流进行系统性的分析。 对于现有作业，必须先重新启动该作业。 

在[此处](https://aka.ms/job_diagram)了解作业关系图。

在作业关系图中检查以下输入指标，帮助解答有关作业从其输入源获取数据的以下针对性问题。 如果查询已分区，请检查每个分区。  

_1) 实际读取了多少数据？_ 

**InputEventsSourcesTotal** 指标提供已读取的数据单位数目，例如 Blob 数目。 <br>
**InputEventsTotal** 提供已读取的事件数目。 此指标按分区提供。 <br>
**InputEventsInBytesTotal** 提供已读取的字节数目。 <br>
**InputEventsLastArrivalTime** 将连同每个已接收事件的排队时间一起更新 

_2) 时间是否在不断前进？如果已读取实际事件，可能不会发出停顿。_ 

**InputEventsLastPunctuationTime** 表示发出停顿、使时间不断前进的时间。 如果不发出停顿，数据流可能会阻塞。 <br>

_3) 输入中是否有任何错误？_ 

**InputEventsEventDataNullTotal** 保存包含 null 数据的事件计数 <br>
**InputEventsSerializerErrorsTotal** 保存无法正确反序列化的事件计数 <br>
**InputEventsDegradedTotal** 保存出现了问题、但该问题不是反序列化问题的事件计数 

_4) 是否正在丢弃/调整事件？_ 

**InputEventsEarlyTotal** 提供在前高水位线之前具有应用程序时间戳的事件数目。 <br>
**InputEventsLateTotal** 提供在前高水位线之后具有应用程序时间戳的事件数目。 <br>
**InputEventsDroppedBeforeApplicationStartTimeTotal** 提供在作业开始时间之前被丢弃的事件数目 

_5) 读取数据的时间是否有滞后？_ 

**InputEventsSourcesBackloggedTotal** 告知还需要为 EventHub 和 IoTHub 输入读取多少条消息。 



<!--HONumber=Nov16_HO1-->



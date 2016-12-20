<properties 
    pageTitle="在作业中看不到任何输入"
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
        * 如果“输入事件数”大于 0，则 ASA 作业可以读取数据。 否则，可能存在以下问题：
            * 如果使用了 Timestamp By，请确保事件中的时间戳大于开始时间。 
            * 使用服务总线资源管理器（如果将事件中心用作输入）查看数据源，确定它是否包含此作业的有效数据 
            * 检查数据序列化格式和编码是否符合预期。 
            * 如果使用事件中心，消息正文可能为 Null。 




<!--HONumber=Dec16_HO3-->



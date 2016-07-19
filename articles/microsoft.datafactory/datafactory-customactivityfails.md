<properties 
    pageTitle="Custom .NET activity fails" 
    description="我的自定义活动不按预期工作或崩溃。" 
    service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="5"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>


# 我的自定义活动不按预期工作或崩溃

## **建议的步骤**

调试包括几种基本方法：

1.  如果输入切片未设置为 **Ready**，确认输入文件夹结构正确，并且输入文件在输入文件夹中存在。 
2.  在自定义活动的 **Execute** 方法中，使用 **IActivityLogger** 对象记录信息以帮助排查问题。 记录的消息将显示在用户日志文件（一个或多个文件，命名为 user-0.log、user-1.log、user-2.log）中。  
3.  将 **PDB** 文件包含在 zip 文件中，这样，在发生错误时，错误详细信息中会提供**调用堆栈**等信息。
4.  在 zip 文件中，用于自定义活动的所有文件必须在不包含任何子文件夹的**顶级**目录中。
5.  确保 **assemblyName** (MyDotNetActivity.dll)、**entryPoint**(MyDotNetActivityNS.MyDotNetActivity)、**packageFile** (customactivitycontainer/MyDotNetActivity.zip) 和 **packageLinkedService**（应指向包含 zip 文件的 Azure Blob 存储）已设置为正确的值。 
6.  如果你解决了错误并想要重新处理切片，请在“OutputDataset”边栏选项卡中右键单击该切片，然后单击“运行”。 
7.  自定义活动不会使用包中的 **app.config** 文件，因此，如果你的代码从配置文件读取任何连接字符串，在运行时，代码将无法正常运行。 使用 Azure Batch 时的最佳做法是在 **Azure KeyVault** 中保存所有机密，使用基于证书的服务主体来保护 **keyvault**，并将该证书分发到 Azure Batch 池。 然后，.NET 自定义活动可以在运行时从 KeyVault 访问机密。 这是一种通用解决方法，可以延伸到任何类型的机密，而不仅仅是连接字符串。

## **建议的文档**
[在 Azure 数据工厂管道中使用自定义活动](https://azure.microsoft.com/documentation/articles/data-factory-use-custom-activities/)


<!--HONumber=Jul16_HO1-->



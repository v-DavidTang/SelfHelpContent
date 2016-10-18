<properties 
    pageTitle="My web application shows Internal Server Error or Service Unavailable (50x)"
    description="Web 应用程序显示“内部服务器错误”或“服务不可用”(50x)"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="jluk"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""  
    productPesIds=""
    cloudEnvironments="public"
/>


# Web 应用程序显示“内部服务器错误”或“服务不可用”(50x)

## **建议的步骤**
这些错误被视为应用程序错误，因此像在任何本地托管的应用程序上一样排查这些错误。  

1.  远程连接到实例，检查是否可以在本地访问 Web 应用程序。 <br> 这样就可以确定该问题是只会在某些实例上出现，还是会在所有实例上出现。

2.  在 IIS 日志中检查失败的具体请求 (50x)。 <br>
这些日志通常位于 *C:\Resources\Directory\guid.role.DiagnosticStore\LogFiles\W3SVC1*。

3.  在发生请求失败的同一个实例上的**“事件查看器”**中查看**“应用程序日志”**；查看有关 HTTP **50x** 错误的详细信息。

4.  在应用程序中添加额外的日志记录。<br>

5.  将一个 **helloworld.html** 测试文件放入 **sitesroot** 文件夹。 <br>
如果任何启动文件（例如 **global.asax** 或 **web.config**）有问题，则访问 **helloworld.html** 时也会出现相同的问题。 这可以帮助确定问题是否与网站本身有关。

6.  在**“IIS”**中启用**“失败请求跟踪”**，查看详细的错误消息。

7.  使用 **DebugView** 捕获异常/错误。

8.  若要进一步诊断，请使用 **[DebugDiag](https://msdn.microsoft.com/library/ff420662.aspx)**、**ProcDump** 或 **WinDbg** 捕获并查看内存转储。 这样就能找到问题所在的线索。



<!--HONumber=Oct16_HO1-->



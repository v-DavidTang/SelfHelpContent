<properties 
    pageTitle="My application is slow"
    description="应用程序速度缓慢"
    service="microsoft.classiccompute"
    resource="domainnames"
    authors="jluk"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""  
    productPesIds=""
    cloudEnvironments="public"
/>


# 应用程序速度缓慢

## **建议的步骤**
1.  将应用程序访问的外部依赖项（SQL Azure、Azure Redis 缓存等）保留在同一个区域。 <br>
如果应用程序具有大量外部资源，网络延迟可能会导致性能下降。
2.  查看操作系统级的指标，例如 CPU、内存使用量、IO 和网络。 <br>
如果任何一项资源的利用率一贯较高，应用程序所需的资源可能会超出当前硬件能够提供的资源。 如果出现资源方面的约束，可以横向或纵向扩展资源。 
3.  查看应用程序的错误日志、跟踪和指标。 <br>
日志、跟踪和指标可以确定是否有任何应用程序瓶颈造成性能问题。 从一次性问题中恢复的快速方法是重新启动应用程序和计算机。
4.  若要进一步诊断，请使用 [DebugDiag](https://msdn.microsoft.com/library/ff420662.aspx)、**ProcDump** 或 **WinDbg**。 <br> 这些程序可捕获内存转储，提供应用程序中问题所在的线索。

## **建议的文档**
[使用分析工具进行故障排除，隔离 CPU 和内存相关的问题](https://channel9.msdn.com/Series/PerfView-Tutorial)<br>
[针对性能瓶颈使用 Perfview 来收集和分析数据](http://www.microsoft.com/download/details.aspx?id=28567)<br>
[使用“调试诊断”排查导致响应停止的进程](https://support.microsoft.com/kb/919792)


<!--HONumber=Oct16_HO2-->



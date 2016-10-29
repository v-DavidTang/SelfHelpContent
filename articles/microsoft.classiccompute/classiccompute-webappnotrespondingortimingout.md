<properties 
    pageTitle="My web application is not responding or timing out"
    description="Web 应用程序无响应或超时"
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


# Web 应用程序无响应或超时

## **建议的步骤**
1.  在 Azure 门户中检查云服务可用性。 <br>
确保所有角色实例处于**“就绪”**状态。 如果不是，请参考故障排除边栏选项卡。
2.  通过 RDP 连接到角色实例，然后在任务管理器中检查应用程序进程 (**w3wp.exe**) 是否正在运行。 <br>
如果 **w3wp.exe** 过程未在任务管理器中显示，请转到 [IIS 管理器] (https://technet.microsoft.com/library/jj635847(v=ws.11).aspx) 并重新启动应用程序。
3.  在浏览器中检查获取的 http 响应代码。 <br>
**50x** 错误是应用程序相关的问题，请参考故障排除边栏选项卡。
4.  检查是否可访问默认端口 **80**（用于 http）和 **443**（用于 https）。 使用 **TELNET** 或 **TCPING** 确保 **w3wp.exe** 进程正在侦听这些端口。 <br>
如果可以在本地访问 Web 应用程序，但无法从外部访问，则问题可能与网络相关。 <br>


<!--HONumber=Oct16_HO2-->



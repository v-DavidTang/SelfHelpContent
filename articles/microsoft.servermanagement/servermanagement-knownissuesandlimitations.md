<properties
    pageTitle="Known issues and limitations"
    description="Server 服务器管理工具的已知问题和限制"
    service="microsoft.servermanagement"
    resource="nodes"
    authors="jol"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# 已知问题和限制
* Nano 服务器<br>
不支持 Nano 服务器的联机域加入和工作组成员身份联机更改。 有关将 Nano 服务器加入到域的说明，请参阅以下主题。<br>
[Nano 服务器入门 - 将 Nano 服务器加入域](https://technet.microsoft.com/en-us/library/mt126167.aspx#Anchor_4)<br>
[Nano 服务器域加入（大规模部署简介）](https://blogs.technet.microsoft.com/privatecloud/2016/05/02/nano-server-domain-join-deployment-at-a-scale-part-1-introduction/) 
* 注册表编辑器<br>
不支持编辑二进制值。
* 服务<br>
对服务执行的任何操作（例如启动或停止服务）将在 10 秒后反映在 UI 中。
* 证书管理器<br>
Windows Server 2016 Technical Preview (TP) 5 Nano 服务器版不支持证书导入和导出。 你将收到一条错误，指出缺少“CertPKICmdlet.dll”。 Nano 服务器 RTM 版将会解决此问题。



<!--HONumber=Jul16_HO3-->



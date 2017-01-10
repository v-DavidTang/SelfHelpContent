<properties 
    pageTitle="使用 Service Fabric Explorer (SFX) (SFX) 或 PowerShell 连接到管理终结点失败 " 
    description="使用 Service Fabric Explorer (SFX) (SFX) 或 PowerShell 连接到管理终结点失败 " 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    displayOrder="8"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="public,BlackForest,Fairfax"   
/>
 

# <a name="connection-failures-using-service-fabric-explorer-sfx-or-powershell-to-the-management-endpoint"></a>使用 Service Fabric Explorer (SFX) (SFX) 或 PowerShell 连接到管理终结点失败 

## <a name="recommended-steps"></a>**建议的步骤**

尝试浏览到 SFX https 终结点（Azure 管理门户中显示的 URL，通常为 https://{群集名称}.{区域}.cloudapp.azure.com:19080/Explorer）。  

1. 如果连接失败，则意味无法向端口 19080 发送 https 流量。
  + 尝试使用 telnet 访问 IP 地址和端口 19080，验证连接是否失败。
  + 确保浏览的是 https 地址，而不是管理终结点的 http 地址。
  + 检查网络安全组是否阻止了流量。
  + 确保群集正在运行，节点在管理门户中可见（请参阅“群集未启动或节点未显示”部分）。 
  + 检查客户端网络问题，例如，代理服务器是否阻止了流量。

2.  如果收到了证书相关的错误，则意味着可以连接到端口 19080，但证书可能存在问题
  + 可能使用了未链接到根 CA 的自签名证书。  可以从证书颁发机构获取签名的证书，或者将自签名证书添加到受信任的根存储。
  + 所用证书的使用者名称可能与浏览到的 DNS 名称不同。  可以设置 DNS 映射（CNAME、A 记录或本地 hosts 文件），将证书使用者名称（例如 servicefabric.mycompany.com）映射到 Service Fabric 管理终结点（例如 mycluster.westus.cloudapp.azure.com）， 然后重试浏览到自定义域名 (https://servicefabric.mycompany.com:19080/Explorer)。
  + 如果信任提供的服务器证书，则可以放心地忽略浏览器中的证书警告并继续访问站点。
  + 连接到受证书保护的群集时，必须提供一个证书用来对客户端进行身份验证。  为此，请确保群集安全证书位于个人证书存储中。  浏览到管理终结点时，Web 浏览器应会提示选择客户端证书，此时，可以从证书存储中选择群集证书。
  + 如果使用 Powershell 进行连接，则需要将群集证书放在个人证书存储中，并且在连接到群集时，需在 Powershell 中指定客户端证书。 
  
## <a name="recommended-documents"></a>**建议的文档**
   [连接到安全群集](https://azure.microsoft.com/documentation/articles/service-fabric-connect-to-secure-cluster/)



<!--HONumber=Jan17_HO1-->



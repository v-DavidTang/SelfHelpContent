<properties
    pageTitle="基础结构设置/Active Directory 联合身份验证配置（STS 和 AD FS）"
    description="基础结构设置/Active Directory 联合身份验证配置（STS 和 AD FS）"
    service="microsoft.remoteapp"
    resource=""
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32335799"
    resourceTags=""
    productPesIds="15540"
    cloudEnvironments="public"
/>


# 基础结构设置/Active Directory 联合身份验证配置（STS 和 AD FS）

## **建议的步骤**
查看以下各项以帮助查明问题。

1. 确保你的映像有效。 如果在等待预配集合时看到一条包含“GoldImageInvalid”的消息，则表示你的映像不符合要求。<br>
[请查看映像要求，并确保使用有效的模板映像。](https://azure.microsoft.com/documentation/articles/remoteapp-imagereqs/)
2. 如果在用于集合的子网上的虚拟网络中定义了网络安全组，请确保可从你的子网内部访问所列的 URL 和端口。<br>
[查看端口和 URL 的列表](https://azure.microsoft.com/documentation/articles/remoteapp-ports/)
3. 如果你使用自己的 DNS 服务器，请确保可从 Azure RemoteApp 虚拟网络子网访问这些服务器。<br>
[请参阅“VM 和角色实例的名称解析”，确保正确配置了 DNS 服务器。](https://azure.microsoft.com/documentation/articles/virtual-networks-name-resolution-for-vms-and-role-instances/)

## **建议的文档**
[排查创建 Azure RemoteApp 混合集合时遇到的问题](https://azure.microsoft.com/documentation/articles/remoteapp-hybridtrouble/)



<!--HONumber=Jul16_HO4-->



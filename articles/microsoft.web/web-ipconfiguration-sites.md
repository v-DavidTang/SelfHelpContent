<properties
    pageTitle="配置和管理/IP 配置"
    description="配置和管理/IP 配置"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32542210"
    resourceTags=""
    productPesIds="14748"
    cloudEnvironments="public"
/>


# 配置和管理/IP 配置

## **建议的步骤**
一个常见的问题是如何获取网站的保留或专用入站 IP 地址。 如果需要配置对 Azure Web 应用站点所发出的入站调用的专用\保留 IP 地址，则需要安装并配置基于 IP 的 SSL 证书。  请注意，若要执行此操作，你的 App Service 计划应位于基本或更高的定价层。 另一个常见问题是如何获取网站 IP 地址。 若要查找出站 IP 地址，请遵循下面列出的步骤：

1. 在 portal.azure.com 上使用新门户浏览到特定 Web 应用的详细信息
2. 在靠近 Web 应用详细信息顶部的位置，有一个“所有设置”链接。 单击该链接。
3. 单击“所有设置”会打开 Web 应用信息列表，你可以在其中进一步深入查看。 要深入到的特定信息为“属性”。 单击“属性”选项。
4. “属性”UX 中有一个显示出站 IP 地址集的文本框。 使用“出站 IP 地址”文本框旁边的图标可以选择所有地址。 按 Ctrl+C 可将地址复制到剪贴板。



<!--HONumber=Jul16_HO4-->



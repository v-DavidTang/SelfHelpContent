<properties 
    pageTitle="How do I specify the ‘service’ and ‘protocol’ for an SRV record?"
    description="如何为 SRV 记录指定“服务”和“协议”？"
    service="microsoft.network"
    resource="dnszones"
    authors="jtuliani"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>


# <a name="how-do-i-specify-the-service-and-protocol-for-an-srv-record"></a>如何为 SRV 记录指定“服务”和“协议”？

## <a name="recommended-steps"></a>**建议的步骤**

Azure DNS 以记录集方式管理记录，记录集是具有相同名称和类型的记录的集合。 对于 SRV 记录集，需将“服务”和“协议”指定为记录集名称的一部分。 对于记录集中的每条记录，需单独指定其他 SRV 参数（“priority”、“weight”、“port”和“target”）。

示例 SRV 记录名称 (service name 'sip', protocol 'tcp')：

- \_sip.\_tcp（在区域顶点创建一个记录集）
- \_sip.\_tcp.sipservice（创建名为“sipservice”的记录集）

## <a name="recommended-documents"></a>**建议的文档**

[DNS zones and records](https://docs.microsoft.com/azure/dns/dns-zones-records)
（DNS 区域和记录）<br>
[Create DNS record sets and records by using the Azure portal](https://docs.microsoft.com/azure/dns/dns-getstarted-create-recordset-portal)
（使用 Azure 门户创建 DNS 记录集和记录）<br>
[SRV 记录类型 (Wikipedia)](https://en.wikipedia.org/wiki/SRV_record)



<!--HONumber=Dec16_HO1-->



<properties 
    pageTitle="I can't create a DNS record"
    description="无法在 Azure DNS 的 DNS 区域创建新 DNS 记录。"
    service="microsoft.network"
    resource="dnszones"
    authors="jtuliani"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>


# <a name="i-cant-create-a-dns-record"></a>无法创建 DNS 记录

## <a name="recommended-steps"></a>**建议的步骤**

若要解决常见问题，请尝试下面的一个或多个步骤：

1.  查看[审核日志](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter)以确定失败原因。
2.  该记录集是否已存在？  Azure DNS 使用记录集管理记录，记录集是具有相同名称和类型的记录的集合。 如果已存在名称和类型相同的记录，那么在添加另一此类记录时，应编辑现有记录集。
3.  希望在 DNS 区域顶点处（该区域的“根”）尝试创建记录？ 如果是这样，DNS 约定会使用 ‘@’ 字符作为记录名称。 另请注意，DNS 标准不允许在区域顶点创建 CNAME 记录。
4.  是否存在 CNAME 冲突？  DNS 标准不允许创建与其他类型记录的名称相同的 CNAME 记录。 如果已存在 CNAME 记录，则无法创建具有相同名称的其他类型的记录。  同样，如果创建的 CNAME 记录与现有其他类型记录的名称相匹配，则无法创建 CNAME 记录。 可通过删除另一条记录或选用不同的记录名称来解决此冲突。
5.  是否已达到 DNS 区域中允许的记录集数量上限？ 在 Azure 门户中此区域的“属性”下，显示有当前记录集数和最大记录集数。 如果已达此限制，则可删除一些记录集或联系 Azure 支持来提高此区域的记录集上限，然后重试。 

如果上述步骤未解决该问题，请将此问题发布到 [MSDN 上的社区支持论坛](https://social.msdn.microsoft.com/Forums/en-US/home?forum=WAVirtualMachinesVirtualNetwork)或创建 Azure 支持请求。

## <a name="recommended-documents"></a>**建议的文档**

[DNS zones and records](https://docs.microsoft.com/azure/dns/dns-zones-records)
（DNS 区域和记录）<br>
[Create DNS record sets and records by using the Azure portal](https://docs.microsoft.com/azure/dns/dns-getstarted-create-recordset-portal)（使用 Azure 门户创建 DNS 记录集和记录）



<!--HONumber=Jan17_HO4-->



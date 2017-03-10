<properties
    pageTitle="How to troubleshoot connectivity or security issue"
    description="如何解决连接或安全问题"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="passaree"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32551655"
    resourceTags=""
    productPesIds="15629"
    cloudEnvironments="public"
/>


# <a name="how-to-troubleshoot-connectivity-or-security-issue"></a>如何解决连接或安全问题
## <a name="recommended-documents"></a>**建议的文档**
### <a name="access-and-connectivity-options"></a>**访问和连接选项**
- [用于管理资源和控制访问的用户策略](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy)
- [将用户访问权限分配给存储帐户](https://azure.microsoft.com/documentation/articles/role-based-access-control-configure/)
- 连接到存储帐户以存储映像：
   - [Microsoft Azure 存储资源管理器](http://storageexplorer.com)
   - [PowerShell](https://azure.microsoft.com/documentation/articles/storage-powershell-guide-full/)
- [Azure 存储连接字符串](https://docs.microsoft.com/azure/storage/storage-configure-connection-string)

### <a name="shared-access-signature-sas"></a>**共享访问签名 (SAS)**
- [何时应使用共享访问签名 (SAS)？](https://docs.microsoft.com/azure/storage/storage-dotnet-shared-access-signature-part-1#when-should-you-use-a-shared-access-signature)
- [如何构造帐户 SAS？](https://docs.microsoft.com/rest/api/storageservices/fileservices/Constructing-an-Account-SAS?redirectedfrom=MSDN)
- [Delegating Access with a Shared Access Signature](https://docs.microsoft.com/rest/api/storageservices/fileservices/delegating-access-with-a-shared-access-signature)（使用共享访问签名委托访问）
- [将 SAS 与存储资源管理器配合使用](https://docs.microsoft.com/azure/vs-azure-tools-storage-manage-with-storage-explorer#attach-storage-account-using-sas)

### <a name="encryption"></a>**加密**
- [传输中加密](https://docs.microsoft.com/azure/storage/storage-security-guide#encryption-in-transit)
- [静态加密](https://docs.microsoft.com/azure/storage/storage-security-guide#encryption-at-rest)
- [将 Azure 磁盘加密或存储服务加密 (SSE) 用于磁盘加密](https://github.com/Microsoft/azure-docs/blob/master/articles/storage/storage-security-guide.md#comparison-of-azure-disk-encryption-sse-and-client-side-encryption)

### <a name="cors"></a>**CORS**
- [启用 CORS 以便应用程序可以在一个域下运行](https://docs.microsoft.com/rest/api/storageservices/fileservices/cross-origin-resource-sharing--cors--support-for-the-azure-storage-services)


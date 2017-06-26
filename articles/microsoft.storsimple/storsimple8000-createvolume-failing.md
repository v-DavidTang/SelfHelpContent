<properties
    pageTitle="I can't create volumes or volume containers"
    description="无法创建卷或卷容器"
    service="microsoft.storsimple"
    resource="managers"
    authors="anbacker"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="8000Series"
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="i-cant-create-volumes-or-volume-containers"></a>无法创建卷或卷容器

如果无法创建卷或卷容器，原因可能是下列其中一项：

## <a name="recommended-steps"></a>**建议的步骤**

* 未正确设置存储帐户。 有关详细说明，请转到[创建新存储帐户](https://docs.microsoft.com/azure/storage/storage-create-storage-account#create-a-storage-account)。
* 存储帐户已被删除。 确保存储帐户仍然存在，并且关联的凭据正确。
* 已重新生成存储帐户访问密钥。 确保可以使用主访问密钥访问存储帐户。 如果已重新生成密钥，需要通过 StorSimple 设备管理器服务同步新密钥。 有关详细说明，请转到[同步存储帐户的密钥](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-storage-accounts#key-rotation-of-storage-accounts)。

## <a name="recommended-documents"></a>**建议的文档**

[用于排查 StorSimple 部署问题的工具](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#tools-for-troubleshooting-storsimple-deployments)<br>
[使用诊断工具排查网络连接问题](https://docs.microsoft.com/azure/storsimple/storsimple-8000-diagnostics)


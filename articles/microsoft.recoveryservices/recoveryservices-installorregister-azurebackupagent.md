<properties
    pageTitle="Azure Recovery Services Agent installation or registration issues"
    description="Azure 恢复服务代理安装或注册问题"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="saurabhsensharma"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds="32447374"
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# Azure 恢复服务代理安装或注册问题

## **建议的步骤**
尝试下面建议的步骤，解决常见的 **Microsoft Azure 恢复服务代理**安装或注册问题

### **安装**
* 确保用于安装 Azure 恢复服务代理的用户帐户是服务器/客户端上**本地管理员**组的成员，或者已被授予管理权限

* 确保 Azure 恢复服务代理的安装目录不带以下属性：<br>
    1. 系统
    2. 已隐藏
    3. 已压缩
    4. 已加密

### **注册**
* 确保 Azure 恢复服务代理所在的 Windows 服务器/客户端上的防火墙设置已配置为允许以下 URL： <br>
    1. www.msftncsi.com
    2. *.Microsoft.com
    3. *.WindowsAzure.com
    4. *.microsoftonline.com
    5. *.windows.net

* 确保安装 Azure 恢复服务代理的服务器/客户端上的**系统时钟**已根据其目标时区设置了正确的时间

* 注册之前确保清除 **C:\Windows\Temp** 目录中的 .tmp 文件

* 如果要**将 Windows 服务器/客户端重新注册**到保管库，请确保提供的加密通行短语与以前将服务器/客户端注册到同一个保管库期间提供的通行短语匹配
 
## **建议的文档**
[Azure 备份常见问题](https://azure.microsoft.com/documentation/articles/backup-azure-backup-faq/)<br>





<!--HONumber=Sep16_HO3-->



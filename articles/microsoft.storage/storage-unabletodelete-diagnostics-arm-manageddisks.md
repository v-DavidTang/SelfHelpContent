<properties
pageTitle="Running VM attached"
description="已附加到正在运行的 VM"
infoBubbleText="已附加到正在运行的 VM"
service="microsoft.storage"
resource="storage"
authors="divka78"
displayOrder=""
articleId="storagedeletionarm_manageddisk"
diagnosticScenario="Classic Image exists"
selfHelpType="diagnostics"
supportTopicIds="32551656"
resourceTags="windows"
productPesIds="15629"
cloudEnvironments="public"
/>


# <a name="running-vm-attached"></a>**已附加到正在运行的 VM**
<!--issueDescription-->

Microsoft Azure 已结束有关删除操作的调查。之所以无法删除磁盘 <!--$disks-->[disks]<!--/$disks-->，是因为它已附加到正在运行的 VM <!--$vmname-->[vmname]<!--/$vmname-->。 只有在停止并删除该 VM 之后，才能删除该磁盘。 <br>
<!--/issueDescription-->


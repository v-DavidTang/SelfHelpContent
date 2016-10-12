<properties 
    pageTitle="Errors deleting a service" 
    description="删除服务时出错" 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="public"   
/>
 

# 删除服务时出错 

## **建议的步骤**
1.  遵循“应用程序/服务的常见失败和故障排除步骤”部分中所述的步骤，确定无法删除服务的原因，以便可以解决应用程序中的任何潜在问题
2.  确定失败原因后，可以结合 -ForceRemove 开关运行 Remove-ServiceFabricReplica，强制删除该服务：
          
```powershell
Connect-ServiceFabricCluster clusterendpoint:19000
$nodes = Get-ServiceFabricNode
foreach($node in $nodes)
{   
$replicas = Get-ServiceFabricDeployedReplica -NodeName $node.NodeName -ApplicationName "fabric:/MyAppName"
 foreach ($replica in $replicas)
 {
 Remove-ServiceFabricReplica -ForceRemove -NodeName $node.NodeName -PartitionId $replica.Partitionid -ReplicaOrInstanceId $replica.ReplicaOrInstanceId
 }
}  
```




<!--HONumber=Sep16_HO4-->



#New-STFEquivalentFarmset
Create a new EquivalentFarmSet for a UserFarmMapping.
##Syntax
```New-STFEquivalentFarmset [-Name] <String> [-AggregationGroupName] <String> [-PrimaryFarms] <String[]> [[-BackupFarms] <String[]>] [-LoadBalanceMode] <Failover | LoadBalanced> [[-FarmsAreIdentical] <Boolean>] [<CommonParameters>]
```
##Detailed Description
An EquivalentFarmSet is a set of PrimaryFarms that provide applications and desktops. When the applications and desktops available from each farm are identical, the experience of using any of them would be equivalent to an end user, so the EquivalentFarmSet should be marked as identical. If any of the farms are not identical the applications and desktops available during enumeration and launch would vary, so the EquivalentFarmSet should be marked as not identical. During enumeration, where the farms are not marked as identical, each is queried in parallel, whereas for farms that are marked as identical, only one is queried. The enumerated resources are de-duplicated according to the AggregationGroupName setting of this and other EquivalentFarmSets available to the same user. During launch, the farms to use are selected by UserFarmMapping, EquivalentFarmSet and AggregationGroupName. Once selected they are ordered and requests are load balanced or failed over between them. EquivalentFarmSets also define BackupFarms, they will only be used should all PrimaryFarms and EquivalentFarmSets with identical AggregationGroupName become unavailable.
##Related Commands
*[New-STFEquivalentFarmset](New-STFEquivalentFarmset)
*[Get-STFUserFarmMapping](Get-STFUserFarmMapping)
*[Clear-STFUserFarmMappings](Clear-STFUserFarmMappings)
*[New-STFUserFarmMappingGroup](New-STFUserFarmMappingGroup)
*[Set-STFUserFarmMapping](Set-STFUserFarmMapping)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Name|The unique Name used to identify the EquivalentFarmSet.|true|false||AggregationGroupName|The AggregationGroupName used to de-duplicate applications and desktops that are available on multiple EquivalentFarmSets. Where multiple EquivalentFarmSets are defined the AggregationGroup will prevent the user seeing the application multiple times if it exists in both places.|true|false||PrimaryFarms|The PrimaryFarms. The farm names should match those defined in the Store service.|true|false||BackupFarms|The BackupFarms. The farm names should match those defined in the Store Service.|false|false||LoadBalanceMode|The load balance mode either Failover or LoadBalanced.|true|false||FarmsAreIdentical|Whether the PrimaryFarms in the EquivalentFarmSet all publish identical resources. Set to true if all resources are identical on all primary farms. Set to false if the deployment has some unique resources per farm.|false|false|##Input Type
###System.String
Parameter Name: The .NET 'System.String' reference type
###System.String
Parameter AggregationGroupName: The .NET 'System.String' reference type
###System.String[]
Parameter PrimaryFarms: The .NET 'System.String' reference type
###System.String[]
Parameter BackupFarms: The .NET 'System.String' reference type
###Citrix.StoreFront.Model.Store.LoadBalanceMode
Parameter LoadBalanceMode: The .NET 'Citrix.StoreFront.Model.Store.LoadBalanceMode' value type
###System.Boolean
Parameter FarmsAreIdentical: The .NET 'System.Boolean' value type
##Return Values
###EquivalentFarmSet
The .NET 'Citrix.StoreFront.Model.Store.EquivalentFarmSet' reference type
##Notes
Must be added to a UserFarmMapping via the Set-STFUserFarmMapping cmdlet before it can be used.
##Examples
###EXAMPLE 1 Create a new EquivalentFarmSet
```$eu1Farmset = New-STFEquivalentFarmset -Name "EU1" -AggregationGroupName "EUUsers" -PrimaryFarms XenApp1, XenApp2 -BackupFarms XenAppBackup -LoadBalanceMode LoadBalanced -FarmsAreIdentical $true
```
REMARKS

Creates a new EquivalentFarmSet with two servers XenApp1 and XenApp2 that are identical and will be load balanced.
Should the primary server fail XenAppBackup will be used.

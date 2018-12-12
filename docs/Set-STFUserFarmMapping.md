# Set-STFUserFarmMapping

Update the Store UserFarmMappings

## Syntax

```
Set-STFUserFarmMapping [-StoreService] <StoreService> [-UserFarmMapping] <UserFarmMapping> [[-GroupMembers] <Hashtable[]>] [[-EquivalentFarmSet] <EquivalentFarmSet[]>] [[-IndexNumber] <Int32>] [[-PassThru] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

A UserFarmMapping is used to configure a specified group of users to use the EquivalentFarmSets defined within the UserFarmMapping. A UserFarmMapping can be used to partition users between defferent XenApp\XenDesktop servers.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The StoreService to which the UserFarmMapping relates.|true|true (ByValue)| |
|UserFarmMapping|The UserFarmMapping to add to the StoreService UserFarmMappings.|true|false| |
|GroupMembers|Assign the UserFarmMapping to the specified GroupMembers.|false|false| |
|EquivalentFarmSet|The EquivalentFarmSets to add to the UserFarmMapping.|false|false| |
|IndexNumber|The position within the UserFarmMappings to insert the suppied UserFarmMapping.|false|false| |
|PassThru|Output the UserFarmMappings saved to the StoreService.|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### Citrix.StoreFront.Model.Store.UserFarmMapping

Parameter UserFarmMapping: The .NET `Citrix.StoreFront.Model.Store.UserFarmMapping` reference type

### System.Collections.Hashtable[]

Parameter GroupMembers: The .NET `System.Collections.Hashtable` reference type

### Citrix.StoreFront.Model.Store.EquivalentFarmSet[]

Parameter EquivalentFarmSet: The .NET `Citrix.StoreFront.Model.Store.EquivalentFarmSet` reference type

### System.Int32

Parameter IndexNumber: The .NET `System.Int32` value type

### System.Management.Automation.SwitchParameter

Parameter PassThru: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### UserFarmMapping

The .NET `Citrix.StoreFront.Model.Store.UserFarmMapping` reference type

## Examples

### EXAMPLE 1 Set Store UserFarmMapping

```
Set-STFUserFarmMapping -UserFarmMapping $userMappingUS -EquivalentFarmSet $us1Farmset
```

**REMARKS**

Update the configured UserFarmMapping for the Store service.

### EXAMPLE 2 Set Store UserFarmMapping 2

```
$store = get-STFStoreService -VirtualPath /Citrix/Store
$userMappingEU = Get-STFStoreUserFarmMapping -StoreService $store -Name "EUUsers"
$eu1Farmset = New-STFEquivalentFarmset -Name "EU1" -AggregationGroupName "EUUsers" -PrimaryFarms XenApp1, XenApp2 -BackupFarms XenAppBackup -LoadBalanceMode LoadBalanced -FarmsAreIdentical $true
$eu2Farmset = New-STFEquivalentFarmset -Name "EU1" -AggregationGroupName "EUUsers" -PrimaryFarms XenApp3, XenApp4 -BackupFarms XenAppBackup -LoadBalanceMode LoadBalanced -FarmsAreIdentical $true
Set-STFUserFarmMapping -UserFarmMapping $userMappingEU -EquivalentFarmSet $us1Farmset, $eu2Farmset
```

**REMARKS**

Update the configured UserFarmMapping $userMappingEU for the Store service.

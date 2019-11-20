# Add-STFUserFarmMapping

Add a new UserFarmMapping to a Store Service.

## Syntax

```
Add-STFUserFarmMapping [-StoreService] <StoreService> [-Name] <String> [-GroupMembers] <Hashtable[]> [-EquivalentFarmSet] <EquivalentFarmSet[]> [[-IndexNumber] <Int32>] [[-PassThru] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

A UserFarmMapping is used to configure a specified group of users to use the EquivalentFarmSets defined within the UserFarmMapping. A UserFarmMapping can be used to partition users between defferent XenApp\XenDesktop servers.

## Related Commands

* [Clear-STFUserFarmMappings](./Clear-STFUserFarmMappings)
* [Set-STFUserFarmMapping](./Set-STFUserFarmMapping)
* [New-STFEquivalentFarmset](./New-STFEquivalentFarmset)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The Store service to add the UserFarmMapping to.|true|true (ByValue)| |
|Name|The unique name used to identify the UserFarmMapping.|true|false| |
|GroupMembers|The Windows groups to which the UserFarmMapping will apply. The default value will assign all users to the UserFarmMapping. The @{"Everyone" = "Everyone"} is equivalent to specifying Domain Users and the Domain Users SID.|true|false| |
|EquivalentFarmSet|The EquivalentFarmSets that will be assigned to the UserFarmMapping.|true|true (ByValue)| |
|IndexNumber|The position within the UserFarmMappings to insert the suppied UserFarmMapping.|false|false| |
|PassThru|Output the UserFarmMappings saved to the StoreService.|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.String

Parameter Name: The .NET `System.String` reference type

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

### EXAMPLE 1 Add a new UserFarmMapping

```
$store = Get-STFStoreService -VirtualPath /Citrix/Store
$eu1Farmset = New-STFEquivalentFarmset -Name "EU1" -AggregationGroupName "EUUsers" -PrimaryFarms XenApp1, XenApp2 -BackupFarms XenAppBackup -LoadBalanceMode LoadBalanced -FarmsAreIdentical $true
Add-STFUserFarmMapping -StoreService $store -Name "EUUsers" -GroupMembers (New-STFUserFarmMappingGroup -AllUsers) -EquivalentFarmSet $eu1Farmset
```

**REMARKS**

Adds a new UserFarmMapping to the /Citrix/Store Store service for all users.

### EXAMPLE 2 Add a new UserFarmMapping 2

```
$store = get-STFStoreService -VirtualPath /Citrix/Store
$eu1Farmset = New-STFEquivalentFarmset -Name "EU1" -AggregationGroupName "EUUsers" -PrimaryFarms XenApp1, XenApp2 -BackupFarms XenAppBackup -LoadBalanceMode LoadBalanced -FarmsAreIdentical $true
Add-STFUserFarmMapping -StoreService $store -Name "EUUsers" -GroupMembers @{"EUGroup1" = "S-1-5-21-7375663-6890924511-1272660413-2944159"} -EquivalentFarmSet $eu1Farmset
```

**REMARKS**

Adds a new UserFarmMapping to the /Citrix/Store Store service for EUGroup1.

### EXAMPLE 3 Add a new UserFarmMapping 3

```
$store = get-STFStoreService -VirtualPath /Citrix/Store
$eu1Farmset = New-STFEquivalentFarmset -Name "EU1" -AggregationGroupName "EUUsers" -PrimaryFarms XenApp1, XenApp2 -BackupFarms XenAppBackup -LoadBalanceMode LoadBalanced -FarmsAreIdentical $true
Add-STFUserFarmMapping -StoreService $store -Name "EUUsers" -GroupMembers (New-STFUserFarmMappingGroup -GroupName "EUGroup1" -AccountSid "S-1-5-21-7375663-6890924511-1272660413-2944159") -EquivalentFarmSet $eu1Farmset
```

**REMARKS**

Adds a new UserFarmMapping to the /Citrix/Store Store service for EUGroup1.

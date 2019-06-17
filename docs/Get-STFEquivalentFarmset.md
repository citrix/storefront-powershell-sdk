# Get-STFEquivalentFarmset

Get the EquivalentFarmSet for a UserFarmMapping

## Syntax

```
Get-STFEquivalentFarmset [-UserFarmMapping] <UserFarmMapping> [[-Name] <String>] [<CommonParameters>]
```

## Detailed Description

Get the EquivalentFarmSets configured for a UserFarmMapping or a specific EquivalentFarmSet matching the supplied name.

## Related Commands

* [New-STFEquivalentFarmset](New-STFEquivalentFarmset.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|UserFarmMapping|The UserFarmMapping to get the EquivalentFarmset from.|true|true (ByValue)| |
|Name|Filter the EquivalentFarmset by name.|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.UserFarmMapping

Parameter UserFarmMapping: The .NET `Citrix.StoreFront.Model.Store.UserFarmMapping` reference type

### System.String

Parameter Name: The .NET `System.String` reference type

## Return Values

### EquivalentFarmSet

The .NET `Citrix.StoreFront.Model.Store.EquivalentFarmSet` reference type

## Examples

### EXAMPLE 1 Get all EquivalentFarmSets

```
Get-STFEquivalentFarmset -UserFarmMapping $UserFarmMapping
```

**REMARKS**

Gets all existing EquivalentFarmSet on the $UserFarmMapping object.

### EXAMPLE 2 Get specific EquivalentFarmSet

```
Get-STFEquivalentFarmset -UserFarmMapping $UserFarmMapping -Name "EUMapping"
```

**REMARKS**

Gets the EUMapping from the UserFarmMapping $UserFarmMapping.

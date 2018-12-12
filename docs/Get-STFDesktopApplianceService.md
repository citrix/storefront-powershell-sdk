# Get-STFDesktopApplianceService

Get Desktop Appliance service

## Syntax

```
Get-STFDesktopApplianceService [[-VirtualPath] <String>] [[-SiteId] <Int64>] [<CommonParameters>]
```

## Detailed Description

Get the Desktop Appliance services that match the supplied IIS site id and virtual path filter.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|VirtualPath|Virtual path filter|false|false| |
|SiteId|IIS site id filter|false|false| |

## Input Type

### System.String

Parameter VirtualPath: The .NET `System.String` reference type

### System.Int64

Parameter SiteId: The .NET `System.Int64` value type

## Return Values

### DesktopApplianceService

A .NET class representing the configuration of a StoreFront Desktop Appliance service

## Examples

### EXAMPLE 1 Get Desktop Appliance services

```
Get-STFDesktopApplianceService
```

**REMARKS**

Get all configured Desktop Appliance services

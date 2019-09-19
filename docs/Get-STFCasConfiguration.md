# Get-STFCasConfiguration

Gets the existing CAS data

## Syntax

```
Get-STFCasConfiguration [[-RoamingService] <RoamingService>] [<CommonParameters>]
```

## Detailed Description

Gets the existing CAS data stored in the roaming web.config of your StoreFront deployment.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|RoamingService|The Roaming service|false|false| |

## Input Type

### Citrix.StoreFront.Model.Roaming.RoamingService

Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service

## Return Values

### None

## Examples

### EXAMPLE 1 Display CAS data

```
Get-STFCasConfiguration
```

**REMARKS**

Returns the existing CAS data stored in the roaming web.config file. This data 

is shared by all Stores.

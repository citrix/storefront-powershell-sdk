# Remove-STFCasConfiguration

Removes the existing CAS data

## Syntax

```
Remove-STFCasConfiguration [[-RoamingService] <RoamingService>] [<CommonParameters>]
```

## Detailed Description

Removes the existing CAS data stored in the roaming web.config of your StoreFront deployment.

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
Remove-STFCasConfiguration
              Get-STFCasConfiguration
```

**REMARKS**

After running Remove-STFCasConfiguration then Get-STFCasConfiguration should 

return nothing.

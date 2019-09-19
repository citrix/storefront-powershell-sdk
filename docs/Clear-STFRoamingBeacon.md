# Clear-STFRoamingBeacon

Clear internal or external roaming beacons

## Syntax

```
Clear-STFRoamingBeacon [-RoamingService] <RoamingService> [[-Internal] <SwitchParameter>] [[-External] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Clear the custom internal or external beacons configured for roaming.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|RoamingService|The Roaming service|true|false| |
|Internal|Clear internal beacons|false|false| |
|External|Clear external beacons|false|false| |

## Input Type

### Citrix.StoreFront.Model.Roaming.RoamingService

Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service

### System.Management.Automation.SwitchParameter

Parameter Internal: The .NET `System.Management.Automation.SwitchParameter` value type

### System.Management.Automation.SwitchParameter

Parameter External: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Clear internal beacon

```
Clear-STFRoamingBeacon -Internal
```

**REMARKS**

Clear the internal custom roaming beacon.

### EXAMPLE 2 Clear external beacons

```
Clear-STFRoamingBeacon -External
```

**REMARKS**

Clear all external custom beacons resetting them to the default.

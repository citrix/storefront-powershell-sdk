# Remove-STFRoamingGateway

Remove a Gateway used for remote access and authentication

## Syntax

```
Remove-STFRoamingGateway [-Gateway] <RoamingGateway> [[-RoamingService] <RoamingService>] [<CommonParameters>]



Remove-STFRoamingGateway [-Name] <String> [[-RoamingService] <RoamingService>] [<CommonParameters>]
```

## Detailed Description

Remove a Gateway from the global list of Gateways and from any Stores that are configured to use it for remote access or authentication.

## Related Commands

* [Add-STFRoamingGateway](Add-STFRoamingGateway.md)
* [Get-STFRoamingGateway](Get-STFRoamingGateway.md)
* [Set-STFRoamingGateway](Set-STFRoamingGateway.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Gateway|Remove the Gateway supplied from the global list|true|true (ByValue)| |
|Name|Remove the Gateway named from the global list|true|true (ByValue)| |
|RoamingService|The Roaming service|false|false| |

## Input Type

### Citrix.StoreFront.Model.Roaming.RoamingGateway

Parameter Gateway: The .NET `Citrix.StoreFront.Model.Roaming.RoamingGateway` reference type

### System.String

Parameter Name: The .NET `System.String` reference type

### Citrix.StoreFront.Model.Roaming.RoamingService

Parameter RoamingService: A .NET class representing the configuration of a StoreFront Roaming service

## Return Values

### None

## Notes

Any existing Store Service objects may be invalidated by this operation and should not be used after calling this Cmdlet.

## Examples

### EXAMPLE 1 Remove Gateway by name

```
Remove-STFRoamingGateway -Gateway "Netscaler10x"
```

**REMARKS**

Removes the Gateway with the matching name.

### EXAMPLE 2 Remove Gateway

```
$gateway = Get-STFRoamingGateway -Name "Netscaler10x"
          Remove - STFRoamingGateway - Gateway $gateway
```

**REMARKS**

Gets the Gateway named "Netscaler10x" from the global list and removes it.

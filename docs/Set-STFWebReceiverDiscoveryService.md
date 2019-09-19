# Set-STFWebReceiverDiscoveryService

Set the WebReceiver Discovery Service options

## Syntax

```
Set-STFWebReceiverDiscoveryService [-WebReceiverService] <WebReceiverService> [-RunDiscoveryAtStart] <Boolean> [<CommonParameters>]
```

## Detailed Description

Set the WebReceiver Discovery Service options.

## Related Commands

* [Get-STFWebReceiverDiscoveryService](Get-STFWebReceiverDiscoveryService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |
|RunDiscoveryAtStart|Run discovery when the WebReceiver Application Pool starts.|true|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### System.Boolean

Parameter RunDiscoveryAtStart: The .NET `System.Boolean` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Set WebReceiver Discovery service options

```
$receiver = Get-STFWebReceiverService
Set-STFWebReceiverAuthenticationManager -WebReceiverService $receiver -RunDiscoveryAtStart $false
```

**REMARKS**

Do not run discovery when the WebReceiver Application Pool starts.

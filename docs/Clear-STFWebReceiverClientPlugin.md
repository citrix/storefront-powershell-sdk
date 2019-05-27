# Clear-STFWebReceiverClientPlugin

Clears the plug-ins definitions configured within the WebReceiver

## Syntax

```
Clear-STFWebReceiverClientPlugin [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```

## Detailed Description

The cmdlet clears the plug-ins definitions as configured within the WebReceiver.

## Related Commands

* [Add-STFWebReceiverClientPlugin](Add-STFWebReceiverClientPlugin.md)
* [Remove-STFWebReceiverClientPlugin](Remove-STFWebReceiverClientPlugin.md)
* [Set-STFWebReceiverClientPlugin](Set-STFWebReceiverClientPlugin.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|WebReceiver service to clear of client plug-ins|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

## Return Values

### None

## Examples

### EXAMPLE 1 Clear client plugins

```
$webReceiver = Get-STFWebReceiverService
Clear-STFWebReceiverClientPlugins -WebReceiverService $webReceiver
```

**REMARKS**

Clear all plug-ins from the only configured WebReceiver service.

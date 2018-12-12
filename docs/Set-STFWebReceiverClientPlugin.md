# Set-STFWebReceiverClientPlugin

Sets the plug-ins definitions configured within the WebReceiver

## Syntax

```
Set-STFWebReceiverClientPlugin [-WebReceiverService] <WebReceiverService> [-ClientPlugin] <ClientPlugin[]> [<CommonParameters>]
```

## Detailed Description

The cmdlet sets the plug-ins definitions as configured within the specified WebReceiver.

## Related Commands

* [New-STFWebReceiverClientPlugin](./New-STFWebReceiverClientPlugin)
* [Clear-STFWebReceiverClientPlugin](./Clear-STFWebReceiverClientPlugin)
* [Add-STFWebReceiverClientPlugin](./Add-STFWebReceiverClientPlugin)
* [Get-STFWebReceiverClientPlugin](./Get-STFWebReceiverClientPlugin)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|WebReceiver service to set the client plug-ins on|true|true (ByValue)| |
|ClientPlugin|The client plug-ins to set|true|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### Citrix.StoreFront.Model.ReceiverForWeb.ClientPlugin[]

Parameter ClientPlugin: The .NET `Citrix.StoreFront.Model.ReceiverForWeb.ClientPlugin` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Set the WebReceiver ClientPlugins

```
$webReceiver = Get-STFWebReceiverService
$plugin = New-STFWebReceiverClientPlugin -Name "NetScaler" `
- Source "/plugins/netscalar/script1.js" `
-Scripts @("/plugins/netscalar/script2.js","/plugins/netscalar/script1.js") `
-Styles @("/plugins/netscalar/script2.css","/plugins/netscalar/script1.css") `
-Parameters @{"param1" = "value1";"param2" = "value2"}
Set-STFWebReceiverClientPlugins -WebReceiverService $webReceiver -ClientPlugin $plugin
```

**REMARKS**

Gets the configured WebReceiver and sets the NetScaler Client plug-in.

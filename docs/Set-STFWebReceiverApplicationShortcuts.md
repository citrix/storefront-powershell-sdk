# Set-STFWebReceiverApplicationShortcuts

Set the WebReceiver application shortcuts

## Syntax

```
Set-STFWebReceiverApplicationShortcuts [-WebReceiverService] <WebReceiverService> [[-PromptForUntrustedShortcuts] <Boolean>] [[-TrustedUrls] <Uri[]>] [[-GatewayUrls] <Uri[]>] [<CommonParameters>]
```

## Detailed Description

Set the WebReceiver trusted Urls for application shortcuts.

## Related Commands

* [Get-STFWebReceiverApplicationShortcuts](./Get-STFWebReceiverApplicationShortcuts)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |
|PromptForUntrustedShortcuts|Display confirmation dialog when Receiver for Web cannot determine if an app shortcut originated from a trusted internal site|false|false| |
|TrustedUrls|List of internal web sites that will provide app shortcuts to users|false|false| |
|GatewayUrls|List of gateways through which shortcuts will be provided to users|false|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### System.Boolean

Parameter PromptForUntrustedShortcuts: The .NET `System.Boolean` value type

### System.Uri[]

Parameter TrustedUrls: The .NET `System.Uri` reference type

### System.Uri[]

Parameter GatewayUrls: The .NET `System.Uri` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Configure the Application Shortcuts

```
$webReceiver = Get-STFWebReceiverService "/Citrix/StoreWeb"
Set-STFWebReceiverApplicationShortcuts -WebReceiverService $webReceiver -TrustedUrls "https://mycompany.net"
```

**REMARKS**

Set the WebReceiver trusted urls for shortcuts that users can launch.

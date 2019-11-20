# Clear-STFWebReceiverSiteStyle

Clears the custom site styles for the site for the non-clasic style

## Syntax

```
Clear-STFWebReceiverSiteStyle [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```

## Detailed Description

This command clears all the custom site style defined using Set-DSSiteStyle.

## Related Commands

* [Get-STFWebReceiverDefaultSiteStyle](./Get-STFWebReceiverDefaultSiteStyle)
* [Set-STFWebReceiverSiteStyle](./Set-STFWebReceiverSiteStyle)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service to clear|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

## Return Values

### None

## Examples

### EXAMPLE 1 Clear the customized site style

```
$webReceiver = Get-STFWebReceiverService
Clear-STFWebReceiverSiteStyle -WebReceiverService $webReceiver
```

**REMARKS**

Clear the customized site style of the only configured Receiver.

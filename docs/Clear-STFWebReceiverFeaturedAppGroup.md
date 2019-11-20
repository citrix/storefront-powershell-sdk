# Clear-STFWebReceiverFeaturedAppGroup

Clears the Featured App groups definitions configured within the Receiver for Web

## Syntax

```
Clear-STFWebReceiverFeaturedAppGroup [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```

## Detailed Description

The cmdlet clears the Featured App groups definitions as configured within the Receiver for Web.

## Related Commands

* [Add-STFWebReceiverFeaturedAppGroup](./Add-STFWebReceiverFeaturedAppGroup)
* [Remove-STFWebReceiverFeaturedAppGroup](./Remove-STFWebReceiverFeaturedAppGroup)
* [New-STFWebReceiverFeaturedAppGroup](./New-STFWebReceiverFeaturedAppGroup)
* [Set-STFWebReceiverFeaturedAppGroup](./Set-STFWebReceiverFeaturedAppGroup)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|WebReceiverService to clear of FeaturedAppGroups|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

## Return Values

### None

## Examples

### EXAMPLE 1 Clear FeaturedAppGroups

```
$webReceiver = Get-STFWebReceiverService
Clear-STFWebReceiverFeaturedAppGroup -WebReceiverService $webReceiver
```

**REMARKS**

Clear FeaturedAppGroups from the only configured WebReceiver.

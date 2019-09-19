# Remove-STFWebReceiverFeaturedAppGroup

Removes the specified Featured App group definition from the WebReceiver

## Syntax

```
Remove-STFWebReceiverFeaturedAppGroup [-WebReceiverService] <WebReceiverService> [-FeaturedAppGroup] <FeaturedAppGroup[]> [<CommonParameters>]
```

## Detailed Description

The cmdlet removes the Featured App group definitions from the WebReceiver service.

## Related Commands

* [Add-STFWebReceiverFeaturedAppGroup](Add-STFWebReceiverFeaturedAppGroup.md)
* [New-STFWebReceiverFeaturedAppGroup](New-STFWebReceiverFeaturedAppGroup.md)
* [Clear-STFWebReceiverFeaturedAppGroup](Clear-STFWebReceiverFeaturedAppGroup.md)
* [Set-STFWebReceiverFeaturedAppGroup](Set-STFWebReceiverFeaturedAppGroup.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service to remove the FeaturedAppGroup from|true|true (ByValue)| |
|FeaturedAppGroup|The FeaturedAppGroup to remove|true|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup[]

Parameter FeaturedAppGroup: The .NET `Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Remove the Worx Suite FeatureAppGroup

```
$webReceiver = Get-STFWebReceiverService
$worxAppGroup = Get-STFWebReceiverFeaturedAppGroup -WebReceiverService $webReceiver | Where-Object { $_.Title -eq "Worx Suite" }
Remove - STFWebReceiverFeaturedAppGroup - WebReceiverService $webReceiver - FeaturedAppGroup $worxAppGroup
```

**REMARKS**

Get the Worx Suite FEaturedAppGroup from WebReceiver and remove it.

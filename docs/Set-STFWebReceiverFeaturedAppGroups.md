# Set-STFWebReceiverFeaturedAppGroups

Sets the Featured App groups within the specified WebReceiver.

## Syntax

```
Set-STFWebReceiverFeaturedAppGroups [-WebReceiverService] <WebReceiverService> [-FeaturedAppGroup] <FeaturedAppGroup[]> [<CommonParameters>]
```

## Detailed Description

Sets the Featured App groups within the specified WebReceiver.


Any existing Featured App groups are replaced with the Featured App groups specified.

## Related Commands

* [New-STFWebReceiverFeaturedAppGroup](./New-STFWebReceiverFeaturedAppGroup)
* [Add-STFWebReceiverFeaturedAppGroup](./Add-STFWebReceiverFeaturedAppGroup)
* [Remove-STFWebReceiverFeaturedAppGroup](./Remove-STFWebReceiverFeaturedAppGroup)
* [Clear-STFWebReceiverFeaturedAppGroup](./Clear-STFWebReceiverFeaturedAppGroup)
* [Set-STFWebReceiverFeaturedAppGroup](./Set-STFWebReceiverFeaturedAppGroup)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|WebReceiver service to set the Featured Application groups on|true|true (ByValue)| |
|FeaturedAppGroup|The Featured Application groups to set|true|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup[]

Parameter FeaturedAppGroup: The .NET `Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Set the Feature Application group

```
$webReceiver = Get-STFWebReceiverService
$group = New-STFWebReceiverFeaturedAppGroup -Title "Worx Suite" `
-Description "Improve productivity with a suite of secure mobile apps made for business." `
-TileId appBundle1 `
-ContentType Keyword `
-Contents Worx
Set-STFWebReceiverFeaturedAppGroups -WebReceiverService $webReceiver -FeaturedAppGroup $group
```

**REMARKS**

Set the Featured Application group for the Worx Suite.

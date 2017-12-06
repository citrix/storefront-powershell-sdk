#Remove-STFWebReceiverFeaturedAppGroup
Removes the specified Featured App group definition from the WebReceiver
##Syntax
```Remove-STFWebReceiverFeaturedAppGroup [-WebReceiverService] <WebReceiverService> [-FeaturedAppGroup] <FeaturedAppGroup[]> [<CommonParameters>]
```
##Detailed Description
The cmdlet removes the Featured App group definitions from the WebReceiver service.
##Related Commands
*[Add-STFWebReceiverFeaturedAppGroup](Add-STFWebReceiverFeaturedAppGroup)
*[New-STFWebReceiverFeaturedAppGroup](New-STFWebReceiverFeaturedAppGroup)
*[Clear-STFWebReceiverFeaturedAppGroup](Clear-STFWebReceiverFeaturedAppGroup)
*[Set-STFWebReceiverFeaturedAppGroup](Set-STFWebReceiverFeaturedAppGroup)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service to remove the FeaturedAppGroup from|true|true (ByValue)||FeaturedAppGroup|The FeaturedAppGroup to remove|true|false|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
###Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup[]
Parameter FeaturedAppGroup: The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.FeaturedAppGroup' reference type
##Return Values
##Examples
###EXAMPLE 1 Remove the Worx Suite FeatureAppGroup
```$webReceiver = Get-STFWebReceiverService
$worxAppGroup = Get-STFWebReceiverFeaturedAppGroup -WebReceiverService $webReceiver | Where-Object { $_.Title -eq "Worx Suite" }
Remove - STFWebReceiverFeaturedAppGroup - WebReceiverService $webReceiver - FeaturedAppGroup $worxAppGroup
```
REMARKS

Get the Worx Suite FEaturedAppGroup from WebReceiver and remove it.

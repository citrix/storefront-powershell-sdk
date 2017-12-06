#Add-STFWebReceiverFeature
Add a feature to the WebReceiver service
##Syntax
```Add-STFWebReceiverFeature [-Name] <String> [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
Add-STFWebReceiverFeature [-FeatureClassId] <Guid> [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
Adds a single feature to the specified WebReceiver service.
##Related Commands
*[Remove-STFWebReceiverFeature](Remove-STFWebReceiverFeature)
*[Get-STFWebReceiverFeature](Get-STFWebReceiverFeature)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Name|The name of the WebReceiver feature.|true|false||FeatureClassId|The type id of the WebReceiver feature.|true|false||WebReceiverService|The WebReceiver service to add the feature to.|true|true (ByValue)|##Input Type
###System.String
Parameter Name: The .NET 'System.String' reference type
###System.Guid
Parameter FeatureClassId: The .NET 'System.Guid' value type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
##Examples
###EXAMPLE 1 Add a WebReceiver feature
```$rfw = Get-STFWebReceiverService -VirtualPath /Citrix/StoreWeb
Add-STFWebReceiverFeature -Name CustomSDK -WebReceiverService $rfw
```
REMARKS

Add the feature "CustomSDK" to the WebReceiver service /Citrix/StoreWeb
###EXAMPLE 2 Add the AuthSDK U2F WebReceiver feature
```$webReceiverPackage = Get-STFPackage | Where-Object { $_.Title -eq "WebReceiver" }
# Get features that can be added to WebReceiver
$webReceiverFeatures = Get-STFPackage | Where-Object { $_.ParentIdentifier -eq $webReceiverPackage.Identifier }
# Verify the U2F Receiver Plugin is installed
$u2f = $webReceiverFeatures | Where-Object { $_.Title -eq "U2FReceiverPlugin" }
if($u2f)
{
    $rfw = Get-STFWebReceiverService -VirtualPath /Citrix/StoreWeb
    Add-STFWebReceiverFeature -Name $u2f.Title -WebReceiverService $rfw
}
```
REMARKS

Add the AuthSDK feature "U2FReceiverPlugin" to the WebReceiver service /Citrix/StoreWeb

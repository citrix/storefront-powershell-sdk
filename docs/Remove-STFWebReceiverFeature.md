#Remove-STFWebReceiverFeature
Remove a feature from the WebReceiver service
##Syntax
```Remove-STFWebReceiverFeature [-Name] <String> [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
Remove-STFWebReceiverFeature [-FeatureInstanceId] <Guid> [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
Remove-STFWebReceiverFeature [-FeatureClassId] <Guid> [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
Removes a single feature from the specified WebReceiver service.
##Related Commands
*[Add-STFWebReceiverFeature](Add-STFWebReceiverFeature)
*[Get-STFWebReceiverFeature](Get-STFWebReceiverFeature)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Name|The name of the WebReceiver feature.|true|false||FeatureInstanceId|The instance id of the WebReceiver feature.|true|false||FeatureClassId|The instance id of the WebReceiver feature.|true|false||WebReceiverService|The WebReceiver service to remove the feature from.|true|true (ByValue)|##Input Type
###System.String
Parameter Name: The .NET 'System.String' reference type
###System.Guid
Parameter FeatureInstanceId: The .NET 'System.Guid' value type
###System.Guid
Parameter FeatureClassId: The .NET 'System.Guid' value type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
##Examples
###EXAMPLE 1 Remove a WebReceiver feature
```$rfw = Get-STFWebReceiverService -VirtualPath /Citrix/StoreWeb
Remove-STFWebReceiverFeature -Name CustomSDK -WebReceiverService $rfw
```
REMARKS

Remove the feature "CustomSDK" from the WebReceiver service /Citrix/StoreWeb
###EXAMPLE 2 Remove the AuthSDK U2F WebReceiver feature
```$webReceiverPackage = Get-STFPackage | Where-Object { $_.Title -eq "WebReceiver" }
# Get features that can be removed from WebReceiver
$webReceiverFeatures = Get-STFPackage | Where-Object { $_.ParentIdentifier -eq $webReceiverPackage.Identifier }
# Verify the U2F Receiver Plugin is installed
$u2f = $webReceiverFeatures | Where-Object { $_.Title -eq "U2FReceiverPlugin" }
if($u2f)
{
    $rfw = Get-STFWebReceiverService -VirtualPath /Citrix/StoreWeb
    Remove-STFWebReceiverFeature -Name $u2f.Title -WebReceiverService $rfw
}
```
REMARKS

Remove the AuthSDK feature "U2FReceiverPlugin" from the WebReceiver service /Citrix/StoreWeb

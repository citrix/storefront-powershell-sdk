#Get-STFWebReceiverFeature
Gets the web receiver features
##Syntax
```Get-STFWebReceiverFeature [[-Name] <String>] [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
Gets the feature instances that have been added to the specified WebReceiver service.
##Related Commands
*[Add-STFWebReceiverFeature](Add-STFWebReceiverFeature)
*[Remove-STFWebReceiverFeature](Remove-STFWebReceiverFeature)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||Name|The name of the WebReceiver feature.|false|false||WebReceiverService|The WebReceiver service for which to list the added features.|true|true (ByValue)|##Input Type
###System.String
Parameter Name: The .NET 'System.String' reference type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
##Examples
###EXAMPLE 1 Get all WebReceiver feature instances.
```$rfw = Get-STFWebReceiverService -VirtualPath /Citrix/StoreWeb
Get-STFWebReceiverFeature -WebReceiverService $rfw
```
###EXAMPLE 2 Get the AuthSDK U2F WebReceiver feature instance.
```$rfw = Get-STFWebReceiverService -VirtualPath /Citrix/StoreWeb
Get-STFWebReceiverFeature -Name U2FReceiverPlugin -WebReceiverService $rfw
```

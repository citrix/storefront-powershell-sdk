#Remove-STFWebReceiverClientPlugin
Remove a WebReceiver client plug-in
##Syntax
```Remove-STFWebReceiverClientPlugin [-WebReceiverService] <WebReceiverService> [-ClientPlugin] <ClientPlugin[]> [<CommonParameters>]
```
##Detailed Description
Remove WebReceiver script and branding customizations.
##Related Commands
*[Add-STFWebReceiverClientPlugin](Add-STFWebReceiverClientPlugin)
*[Get-STFWebReceiverClientPlugin](Get-STFWebReceiverClientPlugin)
*[New-STFWebReceiverClientPlugin](New-STFWebReceiverClientPlugin)
*[Clear-STFWebReceiverClientPlugin](Clear-STFWebReceiverClientPlugin)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|WebReceiver from which the client plug-in will be removed|true|true (ByValue)||ClientPlugin|The ClientPlugin to remove|true|false|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
###Citrix.StoreFront.Model.ReceiverForWeb.ClientPlugin[]
Parameter ClientPlugin: The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.ClientPlugin' reference type
##Return Values
##Examples
###EXAMPLE 1 Remove a client plugin
```$webReceiver = Get-STFWebReceiverService
$plugin = Get-STFWebReceiverClientPlugin -WebReceiverService $webReceiver | Where-Object { $_.Name -eq "NetScaler" }
Remove-STFWebReceiverClientPlugin -WebReceiverService $webReceiver
```
REMARKS

Removes the NetScaler client plug-in from $webReceiver.

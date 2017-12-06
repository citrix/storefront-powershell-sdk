#Remove-STFWebReceiverService
Remove a Receiver for Web service
##Syntax
```Remove-STFWebReceiverService [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
Removes an existing Receiver for Web service.
##Related Commands
*[Get-STFWebReceiverService](Get-STFWebReceiverService)
*[Add-STFWebReceiverService](Add-STFWebReceiverService)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|Receiver for Web to remove|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
##Examples
###EXAMPLE 1 Remove Receiver for Web service
```$rfw = Get-STFWebReceiverService
Remove-STFWebReceiverService -WebReceiverService $rfw
```
REMARKS

Remove the only Receiver for Web service

#Get-STFWebReceiverStrictTransportSecurity
Get the WebReceiver strict transport security settings
##Syntax
```Get-STFWebReceiverStrictTransportSecurity [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
Get the WebReceiver strict transport security settings.
##Related Commands
*[Set-STFWebReceiverStrictTransportSecurity](Set-STFWebReceiverStrictTransportSecurity)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service.|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
###StrictTransportSecurity
The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.StrictTransportSecurity' reference type
##Examples
###EXAMPLE 1 Get strict transport security settings
```Enabled        : False
PolicyDuration : 90.00:00:00
```
REMARKS

Get the WebReceiver strict transport security settings for /Citrix/StoreWeb.

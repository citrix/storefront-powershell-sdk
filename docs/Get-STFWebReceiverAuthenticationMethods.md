#Get-STFWebReceiverAuthenticationMethods
Get the WebReceiver authentication methods
##Syntax
```Get-STFWebReceiverAuthenticationMethods [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
Get a list of the current methods that can be used for authentication.
##Related Commands
*[Set-STFWebReceiverAuthenticationMethods](Set-STFWebReceiverAuthenticationMethods)
*[Get-STFWebReceiverAuthenticationMethodsAvailable](Get-STFWebReceiverAuthenticationMethodsAvailable)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service.|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
###AuthenticationMethods
The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.AuthenticationMethods' reference type
##Examples
###EXAMPLE 1 Get authentication methods
```$webReceiver = Get-STFWebReceiverService "/Citrix/StoreWeb"
Get-STFWebReceiverAuthenticationMethods $webReceiver
```
REMARKS

Get the current WebReceiver authentication methods for /Citrix/StoreWeb.
OUTPUT
```LocationUrl   : Authentication/GetAuthMethods
TokenLifeTime : 08:00:00
Methods       : {ExplicitForms, CitrixAGBasic}
```

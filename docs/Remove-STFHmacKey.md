#Remove-STFHmacKey
Remove a named HMAC key stored from a web service.
##Syntax
```Remove-STFHmacKey [-WebService] <StoreFrontWebService> [-Name] <String> [<CommonParameters>]
```
##Detailed Description
Remove an existing named HMAC key stored from a web service.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebService|The Web Service to remove the HMAC key from.|true|true (ByValue)||Name|The name of the HMAC key.|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.StoreFrontWebService
Parameter WebService: The .NET 'Citrix.StoreFront.Model.StoreFrontWebService' reference type
###System.String
Parameter Name: The .NET 'System.String' reference type
##Return Values
##Examples
###EXAMPLE 1 Remove an existing HMAC key named 'test' from the specified Store service.
```$store = $store = Get-STFStoreService -VirtualPath '/Citrix/Store'
Remove-STFHmacKey -WebService $store -Name 'test'
```
REMARKS

Remove the existing HMAC key named 'test' from the specified Store service.

#Set-STFWebReceiverStrictTransportSecurity
Set the WebReceiver HTTP Strict Transport Security options
##Syntax
```Set-STFWebReceiverStrictTransportSecurity [-WebReceiverService] <WebReceiverService> [[-Enabled] <Boolean>] [[-PolicyDuration] <TimeSpan>] [<CommonParameters>]
```
##Detailed Description
Set the WebReceiver HTTP Strict Transport Security options.
##Related Commands
*[Get-STFWebReceiverStrictTransportSecurity](Get-STFWebReceiverStrictTransportSecurity)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service.|true|true (ByValue)||Enabled|Whether to enable the HTTP Strict Transport Security feature.|false|false||PolicyDuration|The time period for which browsers should apply HSTS to the RfWeb site.|false|false|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
###System.Boolean
Parameter Enabled: The .NET 'System.Boolean' value type
###System.TimeSpan
Parameter PolicyDuration: The .NET 'System.TimeSpan' value type
##Return Values
##Examples
###EXAMPLE 1 Enable WebReceiver HTTP Strict Transport Security
```$receiver = Get-STFWebReceiverService
Set-STFWebReceiverStrictTransportSecurity -WebReceiverService $receiver -Enabled $true
```
REMARKS

Enable the HTTP Strict Transport Security feature on the only WebReceiver service.

#Set-STFWebReceiverCommunication
Set the WebReceiver communication settings
##Syntax
```Set-STFWebReceiverCommunication [-WebReceiverService] <WebReceiverService> [[-Attempts] <Int32>] [[-Timeout] <TimeSpan>] [[-Loopback] <On | Off | OnUsingHttp>] [[-LoopbackPortUsingHttp] <Int32>] [[-ProxyEnabled] <Boolean>] [[-ProxyPort] <Int32>] [[-ProxyProcessName] <String>] [<CommonParameters>]
```
##Detailed Description
Set the communication settings used for the WebReceiver proxy.
##Related Commands
*[Get-STFWebReceiverAuthenticationMethods](Get-STFWebReceiverAuthenticationMethods)
*[Get-STFWebReceiverAuthenticationMethodsAvailable](Get-STFWebReceiverAuthenticationMethodsAvailable)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service.|true|true (ByValue)||Attempts|How many attempts WebReceiver should make to contact StoreFront before it gives up.|false|false||Timeout|Timeout value for communicating with StoreFront.|false|false||Loopback|Whether to use the loopback address for communications with the store service, rather than the actual StoreFront server URL. This can optimize performance in most deployments where the store service and web proxy are located on the same box. if “OnUsingHttp” is used, then HTTP (rather than HTTPS) is always used.|false|false||LoopbackPortUsingHttp|When loopback is set to “OnUsingHttp”, the port number to use for loopback communications.|false|false||ProxyEnabled|Is the communications proxy enabled.|false|false||ProxyPort|The port to use for the communications proxy.|false|false||ProxyProcessName|The name of the process acting as proxy.|false|false|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
###System.Int32
Parameter Attempts: The .NET 'System.Int32' value type
###System.TimeSpan
Parameter Timeout: The .NET 'System.TimeSpan' value type
###Citrix.StoreFront.Model.ReceiverForWeb.LoopbackOption
Parameter Loopback: The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.LoopbackOption' value type
###System.Int32
Parameter LoopbackPortUsingHttp: The .NET 'System.Int32' value type
###System.Boolean
Parameter ProxyEnabled: The .NET 'System.Boolean' value type
###System.Int32
Parameter ProxyPort: The .NET 'System.Int32' value type
###System.String
Parameter ProxyProcessName: The .NET 'System.String' reference type
##Return Values
##Examples
###EXAMPLE 1 Configure the communication timeout
```$webReceiver = Get-STFWebReceiverService "/Citrix/StoreWeb"
Set-STFWebReceiverCommunication -WebReceiverService $webReceiver -Timeout 240
```
REMARKS

Set the current WebReceiver communication timeout to four minutes for /Citrix/StoreWeb.

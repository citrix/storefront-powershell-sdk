#Get-STFWebReceiverStoreProxy
Get the WebReceiver Store Proxy options
##Syntax
```Get-STFWebReceiverStoreProxy [-WebReceiverService] <WebReceiverService> [<CommonParameters>]
```
##Detailed Description
Get the WebReceiver Store Service Proxy client options.
##Related Commands
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WebReceiverService|The WebReceiver service.|true|true (ByValue)|##Input Type
###Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService
Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service
##Return Values
###StoreProxy
The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.StoreProxy' reference type
##Examples
###EXAMPLE 1 Get WebReceiver Store Proxy client options
```$receiver = Get-STFWebReceiverService
Get-STFWebReceiverStoreProxy -WebReceiverService $receiver
```
REMARKS

Get the WebReceiver Store Service Proxy client options of the only configured WebReceiver.
OUTPUT
```SessionsProxy  : ListAvailableUrl : Sessions/ListAvailable
                 DisconnectUrl    : Sessions/Disconnect
                 LogoffUrl        : Sessions/Logoff
ResourcesProxy : ListUrl         : Resources/List
                 ResourceDetails : default
KeepAliveUrl   : Home/KeepAlive
```

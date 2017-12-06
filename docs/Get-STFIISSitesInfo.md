#Get-STFIISSitesInfo
Get the IISSites information
##Syntax
```Get-STFIISSitesInfo [<CommonParameters>]
```
##Detailed Description
Get the IISSites information.
##Related Commands
*[Set-STFWebReceiverApplicationShortcuts](Set-STFWebReceiverApplicationShortcuts)
##Input Type
##Return Values
###IISSites
The .NET 'Citrix.StoreFront.Model.ReceiverForWeb.IISSites' reference type
##Examples
###EXAMPLE 1 Get IISSites information
```$iisSiteInfo = Get-STFIISSitesInfo
```
REMARKS

Get the IISSites information.
OUTPUT
```Name                 : {Default Web Site}
Id                 : {1}
Binding                 : {Citrix.StoreFront.Model.ReceiverForWeb.WebSiteBinding}
Applications                 : {Default Web Site, Configuration, Roaming, AGServices...}
```

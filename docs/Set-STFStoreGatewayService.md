#Set-STFStoreGatewayService
Set the gateway service settings for a Store
##Syntax
```Set-STFStoreGatewayService [-StoreService] <StoreService> [[-Enabled] <Boolean>] [[-CustomerId] <String>] [[-GetGatewayServiceUrl] <String>] [[-PrivateKey] <String>] [[-ServiceName] <String>] [[-InstanceId] <String>] [[-SecureTicketAuthorityUrl] <String>] [[-SecureTicketLifetime] <TimeSpan>] [[-SessionReliability] <Boolean>] [[-IgnoreZones] <String[]>] [[-HandleZones] <String[]>] [[-PassThru] <SwitchParameter>] [<CommonParameters>]
```
##Detailed Description
Set the gateway service settings for a Store.
##Related Commands
*[Get-STFStoreGatewayService](Get-STFStoreGatewayService)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||StoreService|The Store service from which to get the gateway service settings|true|true (ByValue)||Enabled|Enable use of the gateway service|false|false||CustomerId|The CWC customer id|false|false||GetGatewayServiceUrl|The URL of the service used to retrieve gateway address (FQDN)|false|false||PrivateKey|The private key for CWC trust|false|false||ServiceName|The service name for CWC trust|false|false||InstanceId|The instance id for CWC trust|false|false||SecureTicketAuthorityUrl|The URL of the CWC STA service|false|false||SecureTicketLifetime|The lifetime requested for CWC STA service tickets|false|false||SessionReliability|A value indicating whether session reliability should be enabled|false|false||IgnoreZones|A value indicating that the gateway service should not be used for the specified zones|false|false||HandleZones|A value indicating that the gateway service should be used for the specified zones|false|false||PassThru|The result is written to the pipeline|false|false|##Input Type
###Citrix.StoreFront.Model.Store.StoreService
Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service
###System.Boolean
Parameter Enabled: The .NET 'System.Boolean' value type
###System.String
Parameter CustomerId: The .NET 'System.String' reference type
###System.String
Parameter GetGatewayServiceUrl: The .NET 'System.String' reference type
###System.String
Parameter PrivateKey: The .NET 'System.String' reference type
###System.String
Parameter ServiceName: The .NET 'System.String' reference type
###System.String
Parameter InstanceId: The .NET 'System.String' reference type
###System.String
Parameter SecureTicketAuthorityUrl: The .NET 'System.String' reference type
###System.TimeSpan
Parameter SecureTicketLifetime: The .NET 'System.TimeSpan' value type
###System.Boolean
Parameter SessionReliability: The .NET 'System.Boolean' value type
###System.String[]
Parameter IgnoreZones: The .NET 'System.String' reference type
###System.String[]
Parameter HandleZones: The .NET 'System.String' reference type
###System.Management.Automation.SwitchParameter
Parameter PassThru: The .NET 'System.Management.Automation.SwitchParameter' value type
##Return Values
###StoreGateway
The .NET 'Citrix.StoreFront.Model.Store.StoreGateway' reference type
##Examples
###EXAMPLE 1 Set gateway service settings for a Store
```$storeService = Set-STFStoreGatewayServiceSettings -StoreService $storeService -Enabled $True -CustomerId $customerId -GetGatewayServiceUrl https://controlpane/Control/PopDnsAddress -PrivateKey $privateKey -ServiceName StoreFront -SecureTicketAuthorityUrl https://cwcstaservice
```

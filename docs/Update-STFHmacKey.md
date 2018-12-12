# Update-STFHmacKey

Update a named HMAC key stored in a web service.

## Syntax

```
Update-STFHmacKey [-WebService] <StoreFrontWebService> [-Name] <String> [-Key] <String> [<CommonParameters>]
```

## Detailed Description

Update an existing named HMAC key stored in a web service.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebService|The Web Service to get the HMAC key from (Base64 encoded).|true|true (ByValue)| |
|Name|The name of the HMAC key.|true|true (ByValue)| |
|Key|The value of the HMAC key.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.StoreFrontWebService

Parameter WebService: The .NET `Citrix.StoreFront.Model.StoreFrontWebService` reference type

### System.String

Parameter Name: The .NET `System.String` reference type

### System.String

Parameter Key: The .NET `System.String` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Update the existing HMAC key named 'logoffTicket' in the specified Store service.

```
$store = $store = Get-STFStoreService -VirtualPath '/Citrix/Store'
Update-STFHmacKey -WebService $store -Name 'logoffTicket' -Key '6UA064hC8Dx/5/s0irY3Vc+tYUh2d6TqPMjC4Qy1NTtCwusyA39mXJTXXPuLaLI7x2wDhFDrsk0rqSqzjlV5Pw=='
```

**REMARKS**

Update the existing HMAC key named 'logoffTicket' in the specified Store service.

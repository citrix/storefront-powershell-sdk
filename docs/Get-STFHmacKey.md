# Get-STFHmacKey

Get a named HMAC key from a web service.

## Syntax

```
Get-STFHmacKey [-WebService] <StoreFrontWebService> [-Name] <String> [<CommonParameters>]
```

## Detailed Description

Get a named HMAC key from a web service.

## Related Commands


## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebService|The Web Service to get the HMAC key from.|true|true (ByValue)| |
|Name|The name of the HMAC key.|true|true (ByValue)| |

## Input Type

### Citrix.StoreFront.Model.StoreFrontWebService

Parameter WebService: The .NET `Citrix.StoreFront.Model.StoreFrontWebService` reference type

### System.String

Parameter Name: The .NET `System.String` reference type

## Return Values

### String

The .NET `System.String` reference type

## Examples

### EXAMPLE 1 Get the HMAC key named 'logoffTicket' from the specified Store service.

```
$store = $store = Get-STFStoreService -VirtualPath '/Citrix/Store'
Get-STFHmacKey -WebService $store -Name 'logoffTicket'
```

**REMARKS**

Get the HMAC key named 'logoffTicket' from the specified Store service.

**OUTPUT**

```
6UA064hC8Dx/5/s0irY3Vc+tYUh2d6TqPMjC4Qy1NTtCwusyA39mXJTXXPuLaLI7x2wDhFDrsk0rqSqzjlV5Pw==
```

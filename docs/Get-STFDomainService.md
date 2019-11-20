# Get-STFDomainService

Get the Domain Service Service

## Syntax

```
Get-STFDomainService [[-DomainServiceName] <String>] [<CommonParameters>]
```

## Detailed Description

Get the Domain Service. The Domain Service is responsible for authentication with the Windows domain.

## Related Commands

* [Set-STFDomainService](./Set-STFDomainService)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|DomainServiceName|The name of the domain service|false|true (ByValue)| |

## Input Type

### System.String

Parameter DomainServiceName: The .NET `System.String` reference type

## Return Values

### DomainService

The .NET `Citrix.StoreFront.Model.WindowsServices.Domain.DomainService` reference type

## Examples

### EXAMPLE 1 Get Domain Service

```
Get-STFDomainService
```

**REMARKS**

Get the Domain service configuration

**OUTPUT**

```
Name              : DefaultDomainService
KerberosSettings  : DomainHint:
FeatureInstanceId : 9f3bbb87-3c15-4cd6-9d20-0b78682f7126
ConfigurationFile : C:\Program Files\Citrix\Receiver StoreFront\Services\DefaultDomainServices\Citrix.DeliveryServices.
                    DomainServices.ServiceHost.exe.config
TenantId          : 860e9401-39c8-4f2c-928d-34251102b840
```

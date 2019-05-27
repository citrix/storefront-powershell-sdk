# Set-STFDomainService

Update the Domain service

## Syntax

```
Set-STFDomainService [-DomainService] <DomainService> [[-KerberosDomainHint] <String>] [<CommonParameters>]
```

## Detailed Description

Update the configuration of the Domain service.

## Related Commands

* [Get-STFDomainService](Get-STFDomainService.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|DomainService|The Domain Service to configure.|true|true (ByValue)| |
|KerberosDomainHint|The Kerberos domain hint.|false|false| |

## Input Type

### Citrix.StoreFront.Model.WindowsServices.Domain.DomainService

Parameter DomainService: The .NET `Citrix.StoreFront.Model.WindowsServices.Domain.DomainService` reference type

### System.String

Parameter KerberosDomainHint: The .NET `System.String` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Change the Domain service Kerberos domain hint

```
Set-STFDomainService -DomainService "domain.test.com"
```

**REMARKS**

Configure the Domain service with a Kerberos domain hint.

# Remove-STFSessionManagerTrustedIssuer

Removes a session manager trusted issuer object from a store.

## Syntax

```
Remove-STFSessionManagerTrustedIssuer [-StoreService] <StoreService> [-SessionManagerTrustedIssuer] <SessionManagerTrustedIssuer> [<CommonParameters>]
```

## Detailed Description

SessionManagerTrustedIssuers are used to indicate that SAML assertions originating from a session manager are to be trusted if they are signed by the certificate in the trusted issuer.

## Related Commands

* [Add-STFSessionManagerTrustedIssuer](./Add-STFSessionManagerTrustedIssuer)
* [New-STFSessionManagerTrustedIssuer](./New-STFSessionManagerTrustedIssuer)
* [Get-STFStoreService](./Get-STFStoreService)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|The store service that this session manager trusted issuer will be removed from|true|true (ByValue)| |
|SessionManagerTrustedIssuer|The session manager trusted issuer object that is to be added to the store|true|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### Citrix.StoreFront.Model.SessionManager.SessionManagerTrustedIssuer

Parameter SessionManagerTrustedIssuer: The .NET `Citrix.StoreFront.Model.SessionManager.SessionManagerTrustedIssuer` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Remove a session manager trusted issuer from a store.

```
$storeService = Get-STFStoreService
$trustedIssuer = $storeService.SessionManagerSettings.SessionManagerTrustedIssuers | Where-Object {$_.Name -eq 'test issuer'}
Remove-STFSessionManagerTrustedIssuer -StoreService $storeService -SessionManagerTrustedIssuer $trustedIssuer
```

**REMARKS**

Remove a session manager trusted issuer from a store.

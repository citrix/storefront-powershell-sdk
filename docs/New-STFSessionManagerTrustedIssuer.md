# New-STFSessionManagerTrustedIssuer

Create a new in memory SessionManagerTrustedIssuer object that represents a trusted signer of session manager assertions.

## Syntax

```
New-STFSessionManagerTrustedIssuer [-Name] <String> [-Thumbprint] <String> [[-TenantId] <String>] [<CommonParameters>]
```

## Detailed Description

SessionManagerTrustedIssuers are added to the store configuration.

## Related Commands

* [Remove-STFSessionManagerTrustedIssuer](./Remove-STFSessionManagerTrustedIssuer)
* [Add-STFSessionManagerTrustedIssuer](./Add-STFSessionManagerTrustedIssuer)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|Name|The name of this trusted issuer. The name is associated with all claims that are validated by this issuer|true|false| |
|Thumbprint|The certificate thumbprint of the certificate that is used by the session manager to sign SAML assertions bound for this store|true|false| |
|TenantId|Tokens sent to storefront from this trusted issuer must be intended for this TenantId if set|false|false| |

## Input Type

### System.String

Parameter Name: The .NET `System.String` reference type

### System.String

Parameter Thumbprint: The .NET `System.String` reference type

### System.String

Parameter TenantId: The .NET `System.String` reference type

## Return Values

### SessionManagerTrustedIssuer

The .NET `Citrix.StoreFront.Model.SessionManager.SessionManagerTrustedIssuer` reference type

## Examples

### EXAMPLE 1 Add a session manager trusted issuer to a store service.

```
$storeService = Get-STFStoreService
$trustedIssuer = New-STFSessionManagerTrustedIssuer -Thumbprint '9ca5d6dbc06fc48cb0115d337c7b030aba56a835' -Name 'test issuer'
Add-STFSessionManagerTrustedIssuer -StoreService $storeService -SessionManagerTrustedIssuer $trustedIssuer
```

**REMARKS**

Add a session manager trusted issuer to a store service.

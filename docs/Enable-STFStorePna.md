# Enable-STFStorePna

Enable PNA (XenApp Services) for a Store

## Syntax

```
Enable-STFStorePna [-StoreService] <StoreService> [[-AllowUserPasswordChange] <SwitchParameter>] [[-LogonMethod] <Anonymous | Prompt | SSON | Smartcard_SSON | Smartcard_Prompt>] [[-DefaultPnaService] <SwitchParameter>] [<CommonParameters>]
```

## Detailed Description

Enable PNA (XenApp Services) for a Store so it can be accessed clients using the PNA protocol.

## Related Commands

* [Disable-STFStorePna](Disable-STFStorePna.md)
* [Clear-STFDefaultPnaStore](Clear-STFDefaultPnaStore.md)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|StoreService|A Store to be configured to support PNA|true|true (ByValue)| |
|AllowUserPasswordChange|Allow the PNA clients to change password|false|false| |
|LogonMethod|The PNA logon method. A Store supports only one method at a time|false|false| |
|DefaultPnaService|Configure the Store to be the default PNA site hosted at http://example.storefront.com/Citrix/Store/PNAgent/config.xml|false|false| |

## Input Type

### Citrix.StoreFront.Model.Store.StoreService

Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service

### System.Management.Automation.SwitchParameter

Parameter AllowUserPasswordChange: The .NET `System.Management.Automation.SwitchParameter` value type

### Citrix.StoreFront.Model.Store.LogonMethod

Parameter LogonMethod: The .NET `Citrix.StoreFront.Model.Store.LogonMethod` value type

### System.Management.Automation.SwitchParameter

Parameter DefaultPnaService: The .NET `System.Management.Automation.SwitchParameter` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Enable PNA for the only Store

```
$storeService = Get-STFStoreService
Enable-STFStorePna $storeService -AllowUserPasswordChange -DefaultPnaService
```

**REMARKS**

Enable PNA on the only Store, allow users to change password and make it the 

deafult PNA site.

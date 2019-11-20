# Get-STFExplictJsonEndPoints

Gets store information as well as the Explicit Json service endpoint URL for each store.

## Syntax

```
Get-STFExplictJsonEndPoints [<CommonParameters>]
```

## Detailed Description

Gets the store infomration as well as the auth service endpoint URL for each store as an array.

## Related Commands


## Input Type

### 



## Return Values

### ExplicitJsonEndPoint[]

The .NET `Citrix.StoreFront.Authentication.Explicit.ExplicitJsonEndPoint` reference type

## Examples

### EXAMPLE 1 Get the Explicit Json service URL for all stores

```
Get-STFExplictJsonEndpoints
```

**REMARKS**

In this example there are two stores and the Explicit JSON auth URL is returned with each store.

To get further information on the Authentication Service for a store use the Get-STFAuthenticationService cmdlet.

**OUTPUT**

```
ExplicitJsonEndPointUrl                                     Store                  
-----------------------                                     -----                  
https://camamnsad.camam.net/Citrix/storeAuth/ExplicitJson   store: /Citrix/store   
https://camamnsad.camam.net/Citrix/store2Auth/ExplicitJson  store2: /Citrix/store2
```

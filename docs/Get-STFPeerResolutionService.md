# Get-STFPeerResolutionService

Get the Peer Resolution Service

## Syntax

```
Get-STFPeerResolutionService [<CommonParameters>]
```

## Detailed Description

Get the Peer Resolution Service (PNRS). The PNRS is responsible for inter server group network communication forming a peer mesh of StoreFront servers.

## Related Commands


## Input Type

### 



## Return Values

### PeerResolutionService

The .NET `Citrix.StoreFront.Model.WindowsServices.Pnrs.PeerResolutionService` reference type

## Examples

### EXAMPLE 1 Get Peer Resolution Service

```
Get-STFPeerResolutionService
```

**REMARKS**

Get the PNRS service configuration

**OUTPUT**

```
HostedServices                  PeerResolver                   
ConfigurationFile              TenantId                      
--------------                  ------------                   
-----------------              --------                      
{pnrs: Enabled}                 Citrix.StoreFront.Model.Win... C:\Program 
Files\Citrix\Rec... 860e9401-39c8-4f2c-928d-342...
```

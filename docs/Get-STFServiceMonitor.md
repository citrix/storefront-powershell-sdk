# Get-STFServiceMonitor

Get the Service Monitor service

## Syntax

```
Get-STFServiceMonitor [<CommonParameters>]
```

## Detailed Description

Get the Server Monitor service used by NetScaler Gateway to perform health checks.

## Related Commands

* [Set-STFServiceMonitor](Set-STFServiceMonitor.md)

## Input Type

### 



## Return Values

### MonitorService

The .NET `Citrix.StoreFront.Model.WindowsServices.ServiceMonitor.MonitorService` reference type

## Examples

### EXAMPLE 1 Get the Service Monitor service

```
Get-STFServiceMonitor
```

**REMARKS**

Gets the Service Monitor service configuration.

**OUTPUT**

```
HostedServices                ServiceUrl                    ConfigurationFile  
           TenantId
--------------                ----------                    -----------------  
           --------
{serviceMonitorService: En... http://localhost:8000/Stor... C:\Program 
Files\Citrix\Re... 860e9401-39c8-4f2c-928d-34...
```

### EXAMPLE 2 Get the Service Monitor service url

```
(Get-STFServiceMonitor).ServiceUrl.AbsoluteUri
```

**REMARKS**

Gets the Service Monitor listening endpoint used by NetScaler.

**OUTPUT**

```
http://localhost:8000/StorefrontMonitor
```

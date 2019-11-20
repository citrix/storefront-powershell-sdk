# Set-STFServiceMonitor

Update the Service Monitor service

## Syntax

```
Set-STFServiceMonitor [[-ServiceUrl] <Uri>] [<CommonParameters>]
```

## Detailed Description

Update the configuration of the Service Monitor service.

## Related Commands

* [Get-STFServiceMonitor](./Get-STFServiceMonitor)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|ServiceUrl|The ServiceUrl to listen to for incoming requests|false|true (ByValue)| |

## Input Type

### System.Uri

Parameter ServiceUrl: The .NET `System.Uri` reference type

## Return Values

### None

## Examples

### EXAMPLE 1 Change the Service Monitor endpoint

```
Set-STFServiceMonitor -ServiceUrl https://localhost:443/StoreFrontMonitor
```

**REMARKS**

Configure the Service Monitor service to use https over port 443.

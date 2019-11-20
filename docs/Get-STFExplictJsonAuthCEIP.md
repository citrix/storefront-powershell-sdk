# Get-STFExplictJsonAuthCEIP

Get the usage of the Explicit Json services

## Syntax

```powershell
Get-STFExplictJsonAuthCEIP [<CommonParameters>]
```

## Detailed Description

Get the usage of the Explicit Json services for the Customer Experience program

## Related Commands

## Input Type

## Return Values

## String

The .NET 'System.String' reference type

## Examples

### EXAMPLE 1 

Get usage of the Explicit Json services

```powershell
$jsonResultString = Get-STFExplictJsonAuthCEIP
```

### REMARKS 

The response string is an object represented as a JSON format string 

### OUTPUT

```json
{"JSONExplicitAuthCEIP":[{"SuccessCount":182,"FailureCount":0,"AuthServiceUptim
e":3671,"Enabled":true},{"SuccessCount":0,"FailureCount":0,"AuthServiceUptime":
0,"Enabled":true}]}
```
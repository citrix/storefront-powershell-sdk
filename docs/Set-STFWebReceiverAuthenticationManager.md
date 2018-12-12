# Set-STFWebReceiverAuthenticationManager

Set the WebReceiver Authentication Manager options

## Syntax

```
Set-STFWebReceiverAuthenticationManager [-WebReceiverService] <WebReceiverService> [-LoginFormTimeout] <Int32> [<CommonParameters>]
```

## Detailed Description

Set the WebReceiver Authentication Manager client options.

## Related Commands

* [Get-STFWebReceiverAuthenticationManager](./Get-STFWebReceiverAuthenticationManager)

## Parameters

| Name   | Description | Required? | Pipeline Input | Default Value |
| --- | --- | --- | --- | --- |
|WebReceiverService|The WebReceiver service.|true|true (ByValue)| |
|LoginFormTimeout|The WebReceiver login form timeout in minutes.|true|false| |

## Input Type

### Citrix.StoreFront.Model.ReceiverForWeb.WebReceiverService

Parameter WebReceiverService: A .NET class representing the configuration of a StoreFront Web Receiver service

### System.Int32

Parameter LoginFormTimeout: The .NET `System.Int32` value type

## Return Values

### None

## Examples

### EXAMPLE 1 Set WebReceiver Authentication options

```
$receiver = Get-STFWebReceiverService
Set-STFWebReceiverAuthenticationManager -WebReceiverService $receiver -LoginFormTimeout 10
```

**REMARKS**

Set the WebReceiver Authentication Manager options to have a 10 minute login form timeout.

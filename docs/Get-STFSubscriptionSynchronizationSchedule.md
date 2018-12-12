# Get-STFSubscriptionSynchronizationSchedule

Get the subscription synchronization schedule

## Syntax

```
Get-STFSubscriptionSynchronizationSchedule [<CommonParameters>]
```

## Detailed Description

Gets a summary of the current subscription synchronization schedule.

## Related Commands

* [Add-STFSubscriptionSynchronizationSchedule](./Add-STFSubscriptionSynchronizationSchedule)
* [Clear-STFSubscriptionSynchronizationSchedule](./Clear-STFSubscriptionSynchronizationSchedule)

## Input Type

### 



## Return Values

### SynchronizationSchedule

The .NET `Citrix.StoreFront.Model.WindowsServices.SubscriptionStore.SynchronizationSchedule` reference type

## Examples

### EXAMPLE 1 Get the current schedule

```
Get-STFSubscriptionSynchronizationSchedule
```

**REMARKS**

Get the currently configured synchronization schedule.

**OUTPUT**

```
ScheduleName                            Start                                                            IntervalRepeat
------------                            -----                                                            --------------
60 minute interval                      10:00:00                                                                     60
```

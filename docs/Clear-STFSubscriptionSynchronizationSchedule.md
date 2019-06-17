# Clear-STFSubscriptionSynchronizationSchedule

Clear the subscription synchronization schedule

## Syntax

```
Clear-STFSubscriptionSynchronizationSchedule [<CommonParameters>]
```

## Detailed Description

Clear the subscription synchronization schedule configured to pull self service subscription changes from a remote StoreFront group.

## Related Commands

* [Add-STFSubscriptionSynchronizationSchedule](Add-STFSubscriptionSynchronizationSchedule.md)
* [Get-STFSubscriptionSynchronizationSchedule](Get-STFSubscriptionSynchronizationSchedule.md)

## Input Type

### 



## Return Values

### None

## Notes

Restarts the Citrix Subscription Store Service to read new settings.

## Examples

### EXAMPLE 1 Clear synchronization schedules

```
Clear-STFSubscriptionSynchronizationSchedule
```

**REMARKS**

Clear all synchronization schedules.

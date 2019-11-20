#Add-STFSubscriptionSynchronizationSchedule
Add a Subscription Synchronization schedule
##Syntax
```Add-STFSubscriptionSynchronizationSchedule [-RecurringStartTime] <TimeSpan> [[-RecurringInterval] <Int32>] [<CommonParameters>]
Add-STFSubscriptionSynchronizationSchedule [-DailySchedule] <TimeSpan[]> [<CommonParameters>]
```
##Detailed Description
Add a Subscription Synchronization schedule to pull self service subscription changes from a remote StoreFront server group.
##Related Commands
*[Clear-STFSubscriptionSynchronizationSchedule](Clear-STFSubscriptionSynchronizationSchedule)
*[Get-STFSubscriptionSynchronizationSchedule](Get-STFSubscriptionSynchronizationSchedule)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||RecurringStartTime|The earliest time at which the first re-occurring synchronization will commence|true|true (ByValue)||RecurringInterval|Number of minutes between each synchronization|false|false||DailySchedule|Absolute times at which synchronization will occur during a single day|true|false|##Input Type
###System.TimeSpan
Parameter RecurringStartTime: The .NET 'System.TimeSpan' value type
###System.Int32
Parameter RecurringInterval: The .NET 'System.Int32' value type
###System.TimeSpan[]
Parameter DailySchedule: The .NET 'System.TimeSpan' value type
##Return Values
##Notes
Restarts the Citrix Subscription Store Service to read new settings.The schedule can be re-occurring using a specific interval or at specific times of the day, not both.
##Examples
###EXAMPLE 1 Add an hourly synchronization schedule
```Add-STFSubscriptionSynchronizationSchedule -ReccuringStartTime 12:00:00 -ReccuringInterval 60
```
REMARKS

Adds a schedule that will commence at 12:00 and repeat hourly.
###EXAMPLE 2 Add absolute times during the day to synchronize
```Add-STFSubscriptionSynchronizationSchedule -DailySchedule 00:00:00,06:00:00,12:00:00,18:00:00
```
REMARKS

Create a schedule to synchronize four times a day.

#Wait-STFServerGroupJoin
Wait for the Server Group join process to complete
##Syntax
```Wait-STFServerGroupJoin [[-WaitTimeout] <Int32>] [<CommonParameters>]
```
##Detailed Description
Waits for the Server Group join process to complete showing a status bar to indicate activity is ongoing.
##Related Commands
*[Stop-STFServerGroupJoin](Stop-STFServerGroupJoin)
*[Remove-STFServerGroupMember](Remove-STFServerGroupMember)
*[Start-STFServerGroupJoin](Start-STFServerGroupJoin)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||WaitTimeout|The length of time in minutes to wait for the join to complete. The default is to wait indefinitely.|false|false|##Input Type
###System.Int32
Parameter WaitTimeout: The .NET 'System.Int32' value type
##Return Values
##Examples
###EXAMPLE 1 Wait for Join to complete
```Wait-STFServerGroupJoin  -Confirm:$false
```
REMARKS

Wait for the server group join to complete. The command can be terminated before completion using the key combination
CTRL+C.

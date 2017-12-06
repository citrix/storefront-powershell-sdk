#Set-STFStoreSubscriptionsDatabase
Sets the location of the subscription data storage for the specified Store
##Syntax
```Set-STFStoreSubscriptionsDatabase [-ConnectionString] <String> [-StoreService] <StoreService> [<CommonParameters>]
Set-STFStoreSubscriptionsDatabase [-UseLocalStorage] <SwitchParameter> [-StoreService] <StoreService> [<CommonParameters>]
```
##Detailed Description
Sets the connection string for the SQL Server database currently used for subscription data for the specified Store.
##Related Commands
*[Get-STFStoreSubscriptionsDatabase](Get-STFStoreSubscriptionsDatabase)
##Parameters
|Name|Description|Required?|Pipeline Input||--|--|--|--||StoreService|The Store service to set the subscriptions storage for|true|true (ByValue)||ConnectionString|The connection string for a SQL Server database which should be used for subscription data storage|true|false||UseLocalStorage|Specifies that the Store should use StoreFront's default local storage. Local storage is created and managed automatically across all members of the server group|true|false|##Input Type
###Citrix.StoreFront.Model.Store.StoreService
Parameter StoreService: A .NET class representing the configuration of a StoreFront Store service
###System.String
Parameter ConnectionString: The .NET 'System.String' reference type
###System.Management.Automation.SwitchParameter
Parameter UseLocalStorage: The .NET 'System.Management.Automation.SwitchParameter' value type
##Return Values
##Examples
###EXAMPLE 1 Configure Sql database connection
```$store = Get-STFStoreService
Set-STFStoreStoreSubscriptionsDatabase -StoreService $store -ConnectionString 'Server=myServerAddress;Database=myDataBase;User Id=myUsername;Password=myPassword;'
```
REMARKS

Configure the store to use a SQL Server database for subscription data storage.
The connection string in this example specifies the server name, instance name and
database name of the SQL Server database and that StoreFront should using Windows
integrated authentication.The connection string format for SQL Server databases is
described in detail in SQL Server documentation.

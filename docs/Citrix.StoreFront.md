#Citrix.StoreFront
##TOPIC
about_Citrix.StoreFront
##SHORT DESCRIPTION
The Citrix.StoreFront module provides administrative functions for the required StoreFront components.
##COMMAND PREFIX
All commands in this module have 'STF' in their name to denote they are part of the StoreFront product.
##LONG DESCRIPTION
The Citrix.StoreFront PowerShell module enables local administration of StoreFront support components. The Authentication, Store and Receiver for Web services are dependant on the base components to deliver applications, desktops, self-service and authentication. Examples of usage can be found in <InstallPath>\PowerShellSDK\Examples. 

The module provides the following main entities: 

* **RoamingService**: The configuration for accessing StoreFront deployments. External gateways are service access information is stored in this service. 
* **ServerGroup**: The configuration of servers that comprise the StoreFront group. 
* **SubscriptionStoreService**: The Windows service based data store used for storing self-service application and desktop subscriptions.
##Cmdlets

* [Import-STFConfiguration](Import-STFConfiguration)
* [Export-STFConfiguration](Export-STFConfiguration)
* [Unprotect-STFConfigurationExport](Unprotect-STFConfigurationExport)
* [Set-STFDeployment](Set-STFDeployment)
* [Get-STFDeployment](Get-STFDeployment)
* [Add-STFDeployment](Add-STFDeployment)
* [Clear-STFDeployment](Clear-STFDeployment)
* [Set-STFDiagnostics](Set-STFDiagnostics)
* [Set-STFDomainService](Set-STFDomainService)
* [Get-STFDomainService](Get-STFDomainService)
* [Uninstall-STFFeature](Uninstall-STFFeature)
* [Install-STFFeature](Install-STFFeature)
* [Reset-STFFeatureData](Reset-STFFeatureData)
* [Get-STFFeatureState](Get-STFFeatureState)
* [Add-STFFeatureState](Add-STFFeatureState)
* [Remove-STFFeatureState](Remove-STFFeatureState)
* [Set-STFFeatureState](Set-STFFeatureState)
* [New-STFFeatureState](New-STFFeatureState)
* [Get-STFFeatureStateNames](Get-STFFeatureStateNames)
* [New-STFFeatureStateProperty](New-STFFeatureStateProperty)
* [Clear-STFFeatureStates](Clear-STFFeatureStates)
* [Remove-STFHmacKey](Remove-STFHmacKey)
* [Add-STFHmacKey](Add-STFHmacKey)
* [Get-STFHmacKey](Get-STFHmacKey)
* [Update-STFHmacKey](Update-STFHmacKey)
* [Get-STFInstalledFeatures](Get-STFInstalledFeatures)
* [Get-STFPackage](Get-STFPackage)
* [Get-STFPeerResolutionService](Get-STFPeerResolutionService)
* [Wait-STFPublishServerGroupConfiguration](Wait-STFPublishServerGroupConfiguration)
* [Get-STFServerGroup](Get-STFServerGroup)
* [Publish-STFServerGroupConfiguration](Publish-STFServerGroupConfiguration)
* [Start-STFServerGroupJoin](Start-STFServerGroupJoin)
* [Stop-STFServerGroupJoin](Stop-STFServerGroupJoin)
* [Wait-STFServerGroupJoin](Wait-STFServerGroupJoin)
* [Get-STFServerGroupJoinState](Get-STFServerGroupJoinState)
* [Remove-STFServerGroupMember](Remove-STFServerGroupMember)
* [Save-STFService](Save-STFService)
* [Get-STFServiceMonitor](Get-STFServiceMonitor)
* [Set-STFServiceMonitor](Set-STFServiceMonitor)
* [Get-STFVersion](Get-STFVersion)

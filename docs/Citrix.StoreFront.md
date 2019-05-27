# Citrix.StoreFront

## Topic

`about_Citrix.StoreFront`

## Short Description

The Citrix.StoreFront module provides administrative functions for the required StoreFront components. 

## Command Prefix

All commands in this module have 'STF' in their name to denote they are part of the StoreFront product. 

## Long Description

The Citrix.StoreFront PowerShell module enables local administration of StoreFront support components. The Authentication, Store and Receiver for Web services are dependant on the base components to deliver applications, desktops, self-service and authentication. Examples of usage can be found in `<InstallPath>\PowerShellSDK\Examples`.

The module provides the following main entities: 

- **RoamingService**: The configuration for accessing StoreFront deployments. External gateways are service access information is stored in this service. 
- **ServerGroup**: The configuration of servers that comprise the StoreFront group. 
- **SubscriptionStoreService**: The Windows service based data store used for storing self-service application and desktop subscriptions. 

## Cmdlets

- [Import-STFConfiguration](Import-STFConfiguration.md)
- [Export-STFConfiguration](Export-STFConfiguration.md)
- [Unprotect-STFConfigurationExport](Unprotect-STFConfigurationExport.md)
- [Set-STFDeployment](Set-STFDeployment.md)
- [Get-STFDeployment](Get-STFDeployment.md)
- [Add-STFDeployment](Add-STFDeployment.md)
- [Clear-STFDeployment](Clear-STFDeployment.md)
- [Set-STFDiagnostics](Set-STFDiagnostics.md)
- [Set-STFDomainService](Set-STFDomainService.md)
- [Get-STFDomainService](Get-STFDomainService.md)
- [Uninstall-STFFeature](Uninstall-STFFeature.md)
- [Install-STFFeature](Install-STFFeature.md)
- [Reset-STFFeatureData](Reset-STFFeatureData.md)
- [Get-STFFeatureState](Get-STFFeatureState.md)
- [Add-STFFeatureState](Add-STFFeatureState.md)
- [Remove-STFFeatureState](Remove-STFFeatureState.md)
- [Set-STFFeatureState](Set-STFFeatureState.md)
- [New-STFFeatureState](New-STFFeatureState.md)
- [Get-STFFeatureStateNames](Get-STFFeatureStateNames.md)
- [New-STFFeatureStateProperty](New-STFFeatureStateProperty.md)
- [Clear-STFFeatureStates](Clear-STFFeatureStates.md)
- [Remove-STFHmacKey](Remove-STFHmacKey.md)
- [Add-STFHmacKey](Add-STFHmacKey.md)
- [Get-STFHmacKey](Get-STFHmacKey.md)
- [Update-STFHmacKey](Update-STFHmacKey.md)
- [Get-STFInstalledFeatures](Get-STFInstalledFeatures.md)
- [Get-STFPackage](Get-STFPackage.md)
- [Get-STFPeerResolutionService](Get-STFPeerResolutionService.md)
- [Wait-STFPublishServerGroupConfiguration](Wait-STFPublishServerGroupConfiguration.md)
- [Get-STFServerGroup](Get-STFServerGroup.md)
- [Publish-STFServerGroupConfiguration](Publish-STFServerGroupConfiguration.md)
- [Start-STFServerGroupJoin](Start-STFServerGroupJoin.md)
- [Stop-STFServerGroupJoin](Stop-STFServerGroupJoin.md)
- [Wait-STFServerGroupJoin](Wait-STFServerGroupJoin.md)
- [Get-STFServerGroupJoinState](Get-STFServerGroupJoinState.md)
- [Remove-STFServerGroupMember](Remove-STFServerGroupMember.md)
- [Save-STFService](Save-STFService.md)
- [Get-STFServiceMonitor](Get-STFServiceMonitor.md)
- [Set-STFServiceMonitor](Set-STFServiceMonitor.md)
- [Get-STFVersion](Get-STFVersion.md)


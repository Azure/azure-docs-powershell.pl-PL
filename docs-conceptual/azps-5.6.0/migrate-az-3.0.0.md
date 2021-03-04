---
title: Przewodnik migracji modułu Az 3.0.0
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 3.0 modułu Az programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 641804fc0931d29f082ef7057f610beb75d7550a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101882112"
---
# <a name="migration-guide-for-az-300"></a>Przewodnik migracji modułu Az 3.0.0

Ten dokument zawiera opis różnic między wersjami 2.0.0 i 3.0.0 modułu Az

<!-- TOC -->

- [Przewodnik migracji dla AZ 3.0.0](#migration-guide-for-az-300)
  - [Batch](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [Niezgodność z poprzednimi wersjami modułu `Az.Resources`](#previous-version-incompatibility-with-azresources-module)
  - [Środowisko obliczeniowe](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [HDInsight](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [IotHub](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [RecoveryServices](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [Zasoby](#resources)
    - [Niezgodność z poprzednimi wersjami modułu `Az.Batch`](#previous-version-incompatibility-with-azbatch-module)
  - [ServiceFabric](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [Server](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a>Batch

### `Get-AzBatchNodeAgentSku`
- Usunięto polecenie cmdlet `Get-AzBatchNodeAgentSku` i zastąpiono je poleceniem cmdlet `Get-AzBatchSupportedImage`.
- Polecenie cmdlet `Get-AzBatchSupportedImage` zwraca te same dane co polecenie cmdlet `Get-AzBatchNodeAgentSku`, ale w bardziej przyjaznym formacie.
- Teraz są również zwracane nowe obrazy niezweryfikowane. Uwzględniono również dodatkowe informacje na temat właściwości `Capabilities` i `BatchSupportEndOfLife` dla każdego obrazu.

#### <a name="before"></a>Stary adres
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a>Po
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a>Niezgodność poprzedniej wersji z modułem Az.Resources
Wersja 2.0.1 modułu „Az.Batch” jest niezgodna ze starszymi wersjami (wersja 1.7.0 i wcześniejsze) modułu „Az.Resources”.  Spowoduje to brak możliwości importowania wersji 1.7.0 modułu „Az.Resources”, gdy zostanie zaimportowana wersja 2.0.1 modułu „Az.Batch”.  Aby rozwiązać ten problem, zaktualizuj moduł „Az.Resources” do wersji 1.7.1 lub nowszej albo zainstaluj najnowszą wersję modułu „Az”.

## <a name="compute"></a>Obliczenia

### `New-AzDiskConfig`
Parametr `UploadSizeInBytes` jest używany zamiast parametru `DiskSizeGB` dla polecenia cmdlet `New-AzDiskConfig`, gdy opcja CreateOption ma wartość Upload

#### <a name="before"></a>Stary adres
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a>Po
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a>HDInsight

### `Get-AzHDInsightJobOutput`
- Zaktualizowano polecenie cmdlet `Get-AzHDInsightJobOutput` tak, aby obsługiwało szczegółowy dostęp na podstawie ról do klucza magazynu.
- Nie ma to wpływu na użytkowników mających rolę Operator, Współautor lub Właściciel w klastrze usługi HDInsight.
- Użytkownicy mający tylko rolę Czytelnik będą musieli jawnie określać parametr `DefaultStorageAccountKey`.

#### <a name="before"></a>Stary adres
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a>Po
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
W przypadku polecenia cmdlet `Add-AzHDInsightConfigValue` usunięto alias polecenia cmdlet `Add-AzHDInsightConfigValues`.

#### <a name="before"></a>Stary adres
Użycie przestarzałego aliasu
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a>Po
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
Dodano nowe polecenie cmdlet `Disable-AzHDInsightMonitoring`. To polecenie cmdlet umożliwia wyłączenie monitorowania w klastrze usługi HDInsight (zastępuje polecenia cmdlet `Disable-AzHDInsightOperationsManagementSuite` i `Disable-AzHDInsightOMS`).

#### <a name="before"></a>Stary adres
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a>Po
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
Dodano nowe polecenie cmdlet `Enable-AzHDInsightMonitoring`. To polecenie cmdlet umożliwia włączenie monitorowania w klastrze usługi HDInsight (zastępuje polecenia cmdlet `Enable-AzHDInsightOperationsManagementSuite` i `Enable-AzHDInsightOMS`).

#### <a name="before"></a>Stary adres
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a>Po
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
Dodano nowe polecenie cmdlet `Get-AzHDInsightMonitoring`. To polecenie cmdlet umożliwia uzyskanie stanu instalacji monitorowania w klastrze usługi Azure HDInsight (zastępuje polecenia cmdlet `Get-AzHDInsightOperationsManagementSuite` i `Get-AzHDInsightOMS`).

#### <a name="before"></a>Stary adres
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a>Po
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
W przypadku polecenia cmdlet `Get-HDInsightProperty` usunięto alias polecenia cmdlet `Get-AzHDInsightProperties`.

#### <a name="before"></a>Stary adres
Użycie przestarzałego aliasu
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a>Po
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
Usunięto polecenia cmdlet `Grant-AzHDInsightRdpServicesAccess` i `Revoke-AzHDInsightRdpServicesAccess`. Nie są one już potrzebne, ponieważ klastry korzystające z typu systemu operacyjnego Windows nie są obsługiwane. Zamiast tego utwórz klaster korzystający z typu systemu operacyjnego Linux.

### `Remove-AzHDInsightCluster`
Typ danych wyjściowych polecenia cmdlet `Remove-AzHDInsightCluster` został zmieniony z `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` na `bool`.

#### <a name="before"></a>Stary adres
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a>Po
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
Polecenie cmdlet jest przestarzałe. Nie ma dla niego polecenia zastępczego.

### `Set-AzHDInsightGatewayCredential`
Typ danych wyjściowych polecenia cmdlet `Set-AzHDInsightGatewayCredential` został zmieniony z `HttpConnectivitySettings` na `AzureHDInsightGatewaySettings`.



## <a name="iothub"></a>IotHub

### `New-AzIotHubImportDevices`
Ten alias został usunięty. Zamiast niego użyj polecenia cmdlet `New-AzIotHubImportDevice`.

#### <a name="before"></a>Stary adres
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a>Po
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
Ten alias został usunięty. Zamiast niego użyj polecenia cmdlet `New-AzIotHubExportDevice`.

#### <a name="before"></a>Stary adres
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a>Po
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
Parametr `EventHubEndPointName` jest przestarzały i nie został zastąpiony, ponieważ moduł IotHub zawiera tylko jeden wbudowany punkt końcowy („events”), który może obsługiwać komunikaty systemu i urządzeń.

#### <a name="before"></a>Stary adres
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a>Po
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
Parametr `EventHubEndPointName` jest przestarzały i nie został zastąpiony, ponieważ moduł IotHub zawiera tylko jeden wbudowany punkt końcowy („events”), który może obsługiwać komunikaty systemu i urządzeń.

#### <a name="before"></a>Stary adres
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a>Po
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
Parametr `EventHubEndPointName` jest przestarzały i nie został zastąpiony, ponieważ moduł IotHub zawiera tylko jeden wbudowany punkt końcowy („events”), który może obsługiwać komunikaty systemu i urządzeń.

#### <a name="before"></a>Stary adres
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a>Po
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
Parametr `OperationsMonitoringProperties` jest przestarzały i nie został zastąpiony, ponieważ moduł IotHub nie korzysta już z wbudowanego punktu końcowego („operationsMonitoringEvents”).



## <a name="recoveryservices"></a>RecoveryServices

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
Elementy `ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` i `ASRRecoveryPlanGroup.EndGroupActions` zostały usunięte z danych wyjściowych.

### `Get-AzRecoveryServicesAsrRecoveryPlan`
Elementy `ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` i `ASRRecoveryPlanGroup.EndGroupActions` zostały usunięte z danych wyjściowych.

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
Parametr IncludeDiskId został zmieniony w celu obsługi bezpośredniego zapisu na dysku zarządzanym w usłudze Azure Site Recovery.

#### <a name="before"></a>Stary adres
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a>Po
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a>Zasoby

### <a name="previous-version-incompatibility-with-azbatch-module"></a>Niezgodność poprzedniej wersji z modułem Az.Batch
Wersja 1.7.1 modułu „Az.Resources” jest niezgodna ze starszymi wersjami (wersja 1.1.2 i wcześniejsze) modułu „Az.Batch”.  Spowoduje to brak możliwości importowania wersji 1.1.2 modułu „Az.Batch”, gdy zostanie zaimportowana wersja 1.7.1 modułu „Az.Resources”.  Aby rozwiązać ten problem, zaktualizuj moduł „Az.Batch” do wersji 2.0.1 lub nowszej albo zainstaluj najnowszą wersję modułu „Az”.

## <a name="servicefabric"></a>ServiceFabric

### `Add-ServiceFabricApplicationCertificate`
Usunięto polecenie cmdlet `Add-ServiceFabricApplicationCertificate`, ponieważ ten scenariusz jest obsługiwany przez polecenie cmdlet `Add-AzVmssSecret`.

#### <a name="before"></a>Stary adres
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a>Po
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a>Sql

### `Get-AzSqlDatabaseSecureConnectionPolicy`
Zauważ, że bezpieczne połączenie jest przestarzałe i dlatego polecenie zostało usunięte. Parametry połączenia możesz wyświetlić za pomocą bloku bazy danych SQL w witrynie Azure Portal

### `Get-AzSqlDatabaseIndexRecommendations`
Alias `Get-AzSqlDatabaseIndexRecommendations` został usunięty. Zamiast tego użyj polecenia cmdlet `Get-AzSqlDatabaseIndexRecommendation`.

### `Get-AzSqlDatabaseRestorePoints`
Alias `Get-AzSqlDatabaseRestorePoints` został usunięty. Zamiast tego użyj polecenia cmdlet `Get-AzSqlDatabaseRestorePoint`.

### `Get-AzSqlDatabaseAuditing`
- Polecenie cmdlet `Get-AzSqlDatabaseAudit` zastępuje to polecenie cmdlet.
- Typ danych wyjściowych ulega zmianie z istniejącego typu „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” na nowy typ „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel”. Usuwane są właściwości `AuditState`, `StorageAccountName` i `StorageAccountSubscriptionId`.  Skrypty mogą pobierać informacje o koncie magazynu z nowej właściwości `StorageAccountResourceId`.

#### <a name="before"></a>Stary adres
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a>Po
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- Polecenie cmdlet `Set-AzSqlDatabaseAudit` zastępuje to polecenie cmdlet.
- Typ danych wyjściowych ulega zmianie z istniejącego typu „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” na nowy typ „bool”

#### <a name="before"></a>Stary adres
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- Polecenie cmdlet `Get-AzSqlServerAudit` zastępuje to polecenie cmdlet.
- Typ danych wyjściowych ulega zmianie z istniejącego typu „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” na nowy typ „Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel”.  Usunięto właściwości `AuditState`, `StorageAccountName` i `StorageAccountSubscriptionId`.  Skrypty, które używają właściwości `StorageAccountName` i `StorageAccountSubscriptionId`, mogą pobrać te informacje z nowej właściwości `StorageAccountResourceId`.

#### <a name="before"></a>Stary adres
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a>Po
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- Polecenie cmdlet `Set-AzSqlServerAudit` zastępuje to polecenie cmdlet.
- Typ danych wyjściowych ulega zmianie z istniejącego typu „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” na nowy typ „bool”

#### <a name="before"></a>Stary adres
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a>Po
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
Polecenie cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlServerAdvancedThreatProtectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a>Po
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
Polecenie cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a>Po
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
Polecenie cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlServerAdvancedThreatProtectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a>Po
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
Polecenie cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
Polecenie cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a>Po
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
Polecenie cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
Polecenie cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a>Po
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
Polecenie cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
Polecenie cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
Polecenie cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a>Po
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
Polecenie cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
Polecenie cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
Polecenie cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a>Po
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
Polecenie cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
Polecenie cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
Polecenie cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlServerVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a>Po
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
Polecenie cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlServerVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
Polecenie cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSetting`

#### <a name="before"></a>Stary adres
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
Polecenie cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` zostało usunięte i nie zostało zastąpione przez żadne polecenie cmdlet

### `Get-AzSqlServerThreatDetectionPolicy`
Polecenie cmdlet `Get-AzSqlServerThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Get-AzSqlServerThreatDetectionSetting`

#### <a name="before"></a>Stary adres
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a>Po
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
Polecenie cmdlet `Remove-AzSqlServerThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlServerThreatDetectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a>Po
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
Polecenie cmdlet `Set-AzSqlServerThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Update-AzSqlServerThreatDetectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a>Po
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
Polecenie cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Get-AzSqlDatabaseThreatDetectionSetting`

#### <a name="before"></a>Stary adres
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a>Po
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
Polecenie cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Update-AzSqlDatabaseThreatDetectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a>Po
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
Polecenie cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlDatabaseThreatDetectionSetting`

#### <a name="before"></a>Stary adres
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a>Po
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

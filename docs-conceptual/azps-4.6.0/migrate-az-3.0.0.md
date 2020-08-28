---
title: Przewodnik migracji modułu Az 3.0.0
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 3.0 modułu Az programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: 06be35bc3573d00d90a8cf2d822ac051ab72f6bb
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821694"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="d44f4-103">Przewodnik migracji modułu Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="d44f4-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="d44f4-104">Ten dokument zawiera opis różnic między wersjami 2.0.0 i 3.0.0 modułu Az</span><span class="sxs-lookup"><span data-stu-id="d44f4-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="d44f4-105">Przewodnik migracji modułu Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="d44f4-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="d44f4-106">Batch</span><span class="sxs-lookup"><span data-stu-id="d44f4-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="d44f4-107">Niezgodność z poprzednimi wersjami modułu `Az.Resources`</span><span class="sxs-lookup"><span data-stu-id="d44f4-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="d44f4-108">Obliczanie</span><span class="sxs-lookup"><span data-stu-id="d44f4-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="d44f4-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d44f4-109">HDInsight</span></span>](#hdinsight)
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
  - [<span data-ttu-id="d44f4-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="d44f4-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="d44f4-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d44f4-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="d44f4-112">Zasoby</span><span class="sxs-lookup"><span data-stu-id="d44f4-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="d44f4-113">Niezgodność z poprzednimi wersjami modułu `Az.Batch`</span><span class="sxs-lookup"><span data-stu-id="d44f4-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="d44f4-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d44f4-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="d44f4-115">Sql</span><span class="sxs-lookup"><span data-stu-id="d44f4-115">Sql</span></span>](#sql)
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


## <a name="batch"></a><span data-ttu-id="d44f4-116">Batch</span><span class="sxs-lookup"><span data-stu-id="d44f4-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="d44f4-117">Usunięto polecenie cmdlet `Get-AzBatchNodeAgentSku` i zastąpiono je poleceniem cmdlet `Get-AzBatchSupportedImage`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="d44f4-118">Polecenie cmdlet `Get-AzBatchSupportedImage` zwraca te same dane co polecenie cmdlet `Get-AzBatchNodeAgentSku`, ale w bardziej przyjaznym formacie.</span><span class="sxs-lookup"><span data-stu-id="d44f4-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="d44f4-119">Teraz są również zwracane nowe obrazy niezweryfikowane.</span><span class="sxs-lookup"><span data-stu-id="d44f4-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="d44f4-120">Uwzględniono również dodatkowe informacje na temat właściwości `Capabilities` i `BatchSupportEndOfLife` dla każdego obrazu.</span><span class="sxs-lookup"><span data-stu-id="d44f4-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-121">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="d44f4-122">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="d44f4-123">Niezgodność poprzedniej wersji z modułem Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d44f4-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="d44f4-124">Wersja 2.0.1 modułu „Az.Batch” jest niezgodna ze starszymi wersjami (wersja 1.7.0 i wcześniejsze) modułu „Az.Resources”.</span><span class="sxs-lookup"><span data-stu-id="d44f4-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="d44f4-125">Spowoduje to brak możliwości importowania wersji 1.7.0 modułu „Az.Resources”, gdy zostanie zaimportowana wersja 2.0.1 modułu „Az.Batch”.</span><span class="sxs-lookup"><span data-stu-id="d44f4-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="d44f4-126">Aby rozwiązać ten problem, zaktualizuj moduł „Az.Resources” do wersji 1.7.1 lub nowszej albo zainstaluj najnowszą wersję modułu „Az”.</span><span class="sxs-lookup"><span data-stu-id="d44f4-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="d44f4-127">Compute</span><span class="sxs-lookup"><span data-stu-id="d44f4-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="d44f4-128">Parametr `UploadSizeInBytes` jest używany zamiast parametru `DiskSizeGB` dla polecenia cmdlet `New-AzDiskConfig`, gdy opcja CreateOption ma wartość Upload</span><span class="sxs-lookup"><span data-stu-id="d44f4-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-129">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="d44f4-130">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="d44f4-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d44f4-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="d44f4-132">Zaktualizowano polecenie cmdlet `Get-AzHDInsightJobOutput` tak, aby obsługiwało szczegółowy dostęp na podstawie ról do klucza magazynu.</span><span class="sxs-lookup"><span data-stu-id="d44f4-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="d44f4-133">Nie ma to wpływu na użytkowników mających rolę Operator, Współautor lub Właściciel w klastrze usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d44f4-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="d44f4-134">Użytkownicy mający tylko rolę Czytelnik będą musieli jawnie określać parametr `DefaultStorageAccountKey`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-135">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="d44f4-136">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="d44f4-137">W przypadku polecenia cmdlet `Add-AzHDInsightConfigValue` usunięto alias polecenia cmdlet `Add-AzHDInsightConfigValues`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-138">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-138">Before</span></span>
<span data-ttu-id="d44f4-139">Użycie przestarzałego aliasu</span><span class="sxs-lookup"><span data-stu-id="d44f4-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="d44f4-140">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="d44f4-141">Dodano nowe polecenie cmdlet `Disable-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="d44f4-142">To polecenie cmdlet umożliwia wyłączenie monitorowania w klastrze usługi HDInsight (zastępuje polecenia cmdlet `Disable-AzHDInsightOperationsManagementSuite` i `Disable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="d44f4-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-143">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="d44f4-144">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="d44f4-145">Dodano nowe polecenie cmdlet `Enable-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="d44f4-146">To polecenie cmdlet umożliwia włączenie monitorowania w klastrze usługi HDInsight (zastępuje polecenia cmdlet `Enable-AzHDInsightOperationsManagementSuite` i `Enable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="d44f4-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-147">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="d44f4-148">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="d44f4-149">Dodano nowe polecenie cmdlet `Get-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="d44f4-150">To polecenie cmdlet umożliwia uzyskanie stanu instalacji monitorowania w klastrze usługi Azure HDInsight (zastępuje polecenia cmdlet `Get-AzHDInsightOperationsManagementSuite` i `Get-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="d44f4-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-151">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="d44f4-152">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="d44f4-153">W przypadku polecenia cmdlet `Get-HDInsightProperty` usunięto alias polecenia cmdlet `Get-AzHDInsightProperties`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-154">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-154">Before</span></span>
<span data-ttu-id="d44f4-155">Użycie przestarzałego aliasu</span><span class="sxs-lookup"><span data-stu-id="d44f4-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="d44f4-156">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="d44f4-157">Usunięto polecenia cmdlet `Grant-AzHDInsightRdpServicesAccess` i `Revoke-AzHDInsightRdpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="d44f4-158">Nie są one już potrzebne, ponieważ klastry korzystające z typu systemu operacyjnego Windows nie są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="d44f4-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="d44f4-159">Zamiast tego utwórz klaster korzystający z typu systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="d44f4-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="d44f4-160">Typ danych wyjściowych polecenia cmdlet `Remove-AzHDInsightCluster` został zmieniony z `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` na `bool`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-161">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="d44f4-162">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="d44f4-163">Polecenie cmdlet jest przestarzałe.</span><span class="sxs-lookup"><span data-stu-id="d44f4-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="d44f4-164">Nie ma dla niego polecenia zastępczego.</span><span class="sxs-lookup"><span data-stu-id="d44f4-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="d44f4-165">Typ danych wyjściowych polecenia cmdlet `Set-AzHDInsightGatewayCredential` został zmieniony z `HttpConnectivitySettings` na `AzureHDInsightGatewaySettings`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="d44f4-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="d44f4-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="d44f4-167">Ten alias został usunięty. Zamiast niego użyj polecenia cmdlet `New-AzIotHubImportDevice`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-168">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="d44f4-169">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="d44f4-170">Ten alias został usunięty. Zamiast niego użyj polecenia cmdlet `New-AzIotHubExportDevice`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-171">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="d44f4-172">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="d44f4-173">Parametr `EventHubEndPointName` jest przestarzały i nie został zastąpiony, ponieważ moduł IotHub zawiera tylko jeden wbudowany punkt końcowy („events”), który może obsługiwać komunikaty systemu i urządzeń.</span><span class="sxs-lookup"><span data-stu-id="d44f4-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-174">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="d44f4-175">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="d44f4-176">Parametr `EventHubEndPointName` jest przestarzały i nie został zastąpiony, ponieważ moduł IotHub zawiera tylko jeden wbudowany punkt końcowy („events”), który może obsługiwać komunikaty systemu i urządzeń.</span><span class="sxs-lookup"><span data-stu-id="d44f4-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-177">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="d44f4-178">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="d44f4-179">Parametr `EventHubEndPointName` jest przestarzały i nie został zastąpiony, ponieważ moduł IotHub zawiera tylko jeden wbudowany punkt końcowy („events”), który może obsługiwać komunikaty systemu i urządzeń.</span><span class="sxs-lookup"><span data-stu-id="d44f4-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-180">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="d44f4-181">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="d44f4-182">Parametr `OperationsMonitoringProperties` jest przestarzały i nie został zastąpiony, ponieważ moduł IotHub nie korzysta już z wbudowanego punktu końcowego („operationsMonitoringEvents”).</span><span class="sxs-lookup"><span data-stu-id="d44f4-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="d44f4-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d44f4-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="d44f4-184">Elementy `ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` i `ASRRecoveryPlanGroup.EndGroupActions` zostały usunięte z danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d44f4-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="d44f4-185">Elementy `ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` i `ASRRecoveryPlanGroup.EndGroupActions` zostały usunięte z danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d44f4-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="d44f4-186">Parametr IncludeDiskId został zmieniony w celu obsługi bezpośredniego zapisu na dysku zarządzanym w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d44f4-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-187">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="d44f4-188">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="d44f4-189">Zasoby</span><span class="sxs-lookup"><span data-stu-id="d44f4-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="d44f4-190">Niezgodność poprzedniej wersji z modułem Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d44f4-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="d44f4-191">Wersja 1.7.1 modułu „Az.Resources” jest niezgodna ze starszymi wersjami (wersja 1.1.2 i wcześniejsze) modułu „Az.Batch”.</span><span class="sxs-lookup"><span data-stu-id="d44f4-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="d44f4-192">Spowoduje to brak możliwości importowania wersji 1.1.2 modułu „Az.Batch”, gdy zostanie zaimportowana wersja 1.7.1 modułu „Az.Resources”.</span><span class="sxs-lookup"><span data-stu-id="d44f4-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="d44f4-193">Aby rozwiązać ten problem, zaktualizuj moduł „Az.Batch” do wersji 2.0.1 lub nowszej albo zainstaluj najnowszą wersję modułu „Az”.</span><span class="sxs-lookup"><span data-stu-id="d44f4-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="d44f4-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d44f4-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="d44f4-195">Usunięto polecenie cmdlet `Add-ServiceFabricApplicationCertificate`, ponieważ ten scenariusz jest obsługiwany przez polecenie cmdlet `Add-AzVmssSecret`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-196">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="d44f4-197">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="d44f4-198">Sql</span><span class="sxs-lookup"><span data-stu-id="d44f4-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="d44f4-199">Zauważ, że bezpieczne połączenie jest przestarzałe i dlatego polecenie zostało usunięte.</span><span class="sxs-lookup"><span data-stu-id="d44f4-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="d44f4-200">Parametry połączenia możesz wyświetlić za pomocą bloku bazy danych SQL w witrynie Azure Portal</span><span class="sxs-lookup"><span data-stu-id="d44f4-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="d44f4-201">Alias `Get-AzSqlDatabaseIndexRecommendations` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="d44f4-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="d44f4-202">Zamiast tego użyj polecenia cmdlet `Get-AzSqlDatabaseIndexRecommendation`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="d44f4-203">Alias `Get-AzSqlDatabaseRestorePoints` został usunięty.</span><span class="sxs-lookup"><span data-stu-id="d44f4-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="d44f4-204">Zamiast tego użyj polecenia cmdlet `Get-AzSqlDatabaseRestorePoint`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="d44f4-205">Polecenie cmdlet `Get-AzSqlDatabaseAudit` zastępuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d44f4-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="d44f4-206">Typ danych wyjściowych ulega zmianie z istniejącego typu „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” na nowy typ „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel”. Usuwane są właściwości `AuditState`, `StorageAccountName`</span><span class="sxs-lookup"><span data-stu-id="d44f4-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="d44f4-207">i `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="d44f4-208">Skrypty mogą pobierać informacje o koncie magazynu z nowej właściwości `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-209">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-209">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="d44f4-210">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-210">After</span></span>
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
- <span data-ttu-id="d44f4-211">Polecenie cmdlet `Set-AzSqlDatabaseAudit` zastępuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d44f4-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="d44f4-212">Typ danych wyjściowych ulega zmianie z istniejącego typu „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” na nowy typ „bool”</span><span class="sxs-lookup"><span data-stu-id="d44f4-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-213">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-214">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="d44f4-215">Polecenie cmdlet `Get-AzSqlServerAudit` zastępuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d44f4-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="d44f4-216">Typ danych wyjściowych ulega zmianie z istniejącego typu „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” na nowy typ „Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel”.</span><span class="sxs-lookup"><span data-stu-id="d44f4-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="d44f4-217">Usunięto właściwości `AuditState`, `StorageAccountName` i `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="d44f4-218">Skrypty, które używają właściwości `StorageAccountName` i `StorageAccountSubscriptionId`, mogą pobrać te informacje z nowej właściwości `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="d44f4-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-219">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-219">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="d44f4-220">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-220">After</span></span>
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
- <span data-ttu-id="d44f4-221">Polecenie cmdlet `Set-AzSqlServerAudit` zastępuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d44f4-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="d44f4-222">Typ danych wyjściowych ulega zmianie z istniejącego typu „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel” na nowy typ „bool”</span><span class="sxs-lookup"><span data-stu-id="d44f4-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-223">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="d44f4-224">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="d44f4-225">Polecenie cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-226">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-227">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="d44f4-228">Polecenie cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-229">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-230">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="d44f4-231">Polecenie cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-232">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="d44f4-233">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="d44f4-234">Polecenie cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-235">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-236">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="d44f4-237">Polecenie cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-238">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="d44f4-239">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="d44f4-240">Polecenie cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-241">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-242">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="d44f4-243">Polecenie cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-244">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-244">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="d44f4-245">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-245">After</span></span>
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
<span data-ttu-id="d44f4-246">Polecenie cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-247">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-248">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="d44f4-249">Polecenie cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-250">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-251">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="d44f4-252">Polecenie cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-253">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-253">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="d44f4-254">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-254">After</span></span>
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
<span data-ttu-id="d44f4-255">Polecenie cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-256">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-257">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="d44f4-258">Polecenie cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-259">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-260">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="d44f4-261">Polecenie cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-262">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-262">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="d44f4-263">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-263">After</span></span>
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
<span data-ttu-id="d44f4-264">Polecenie cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-265">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-266">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="d44f4-267">Polecenie cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-268">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-269">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="d44f4-270">Polecenie cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Update-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-271">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-271">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="d44f4-272">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-272">After</span></span>
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
<span data-ttu-id="d44f4-273">Polecenie cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Get-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-274">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-275">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="d44f4-276">Polecenie cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-277">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-278">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="d44f4-279">Polecenie cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` zostało usunięte i nie zostało zastąpione przez żadne polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="d44f4-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="d44f4-280">Polecenie cmdlet `Get-AzSqlServerThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Get-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-281">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-281">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="d44f4-282">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-282">After</span></span>
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
<span data-ttu-id="d44f4-283">Polecenie cmdlet `Remove-AzSqlServerThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-284">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-285">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="d44f4-286">Polecenie cmdlet `Set-AzSqlServerThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Update-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-287">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="d44f4-288">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="d44f4-289">Polecenie cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Get-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-290">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-290">Before</span></span>
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

#### <a name="after"></a><span data-ttu-id="d44f4-291">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-291">After</span></span>
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
<span data-ttu-id="d44f4-292">Polecenie cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Update-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-293">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="d44f4-294">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="d44f4-295">Polecenie cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` zostało zastąpione przez polecenie cmdlet `Clear-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="d44f4-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="d44f4-296">Przed</span><span class="sxs-lookup"><span data-stu-id="d44f4-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="d44f4-297">Po</span><span class="sxs-lookup"><span data-stu-id="d44f4-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
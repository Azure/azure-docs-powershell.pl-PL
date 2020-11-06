---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e6145ee1773a0ecee3ebb1f8c9b5b9e2386cf229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524318"
---
# <span data-ttu-id="80156-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="80156-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="80156-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80156-102">SYNOPSIS</span></span>
<span data-ttu-id="80156-103">Tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80156-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80156-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80156-104">SYNTAX</span></span>

### <span data-ttu-id="80156-105">HyperVToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80156-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80156-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="80156-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80156-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="80156-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80156-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="80156-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80156-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="80156-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80156-110">Opis</span><span class="sxs-lookup"><span data-stu-id="80156-110">DESCRIPTION</span></span>
<span data-ttu-id="80156-111">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrPolicy** tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80156-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="80156-112">Zasady replikacji są używane do określania ustawień replikacji, takich jak częstotliwość replikacji i liczba punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="80156-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="80156-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80156-113">EXAMPLES</span></span>

### <span data-ttu-id="80156-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80156-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="80156-115">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="80156-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="80156-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="80156-116">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="80156-117">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="80156-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="80156-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="80156-118">Example 3</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="80156-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="80156-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="80156-120">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="80156-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="80156-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80156-121">PARAMETERS</span></span>

### <span data-ttu-id="80156-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="80156-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="80156-123">Określa częstotliwość (w godzinach) tworzenia spójnych punktów odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="80156-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-124">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="80156-124">-Authentication</span></span>
<span data-ttu-id="80156-125">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="80156-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="80156-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="80156-126">Valid values are:</span></span>

- <span data-ttu-id="80156-127">Dyplom</span><span class="sxs-lookup"><span data-stu-id="80156-127">Certificate</span></span>
-  <span data-ttu-id="80156-128">Mechanizmu</span><span class="sxs-lookup"><span data-stu-id="80156-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="80156-129">-AzureToAzure</span></span>
<span data-ttu-id="80156-130">Parametr Switch określający, że tworzone zasady replikacji będą używane do replikowania maszyn wirtualnych platformy Azure między dwoma regionami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80156-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="80156-131">-AzureToVMware</span></span>
<span data-ttu-id="80156-132">Parametr Switch wskazujący, że tworzone zasady replikacji będą używane do wycofywania replikacji na maszynach wirtualnych VMware i serwerach fizycznych uruchomionych na platformie Azure z powrotem do lokalnej witryny programu VMware.</span><span class="sxs-lookup"><span data-stu-id="80156-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="80156-133">-Compression</span></span>
<span data-ttu-id="80156-134">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="80156-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80156-135">-DefaultProfile</span></span>
<span data-ttu-id="80156-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80156-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-137">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="80156-137">-Encryption</span></span>
<span data-ttu-id="80156-138">{{Opis szyfrowania wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="80156-138">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-139">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="80156-139">-HyperVToAzure</span></span>
<span data-ttu-id="80156-140">Parametr Przełącz określający zasady do replikowania maszyn wirtualnych funkcji Hyper-V na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="80156-140">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="80156-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="80156-142">Określa stan synchronizacji multiVm dla zasad.</span><span class="sxs-lookup"><span data-stu-id="80156-142">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80156-143">-Name</span></span>
<span data-ttu-id="80156-144">Określa nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="80156-144">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-145">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="80156-145">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="80156-146">Określa punkty odzyskiwania liczb, które mają zostać zachowane.</span><span class="sxs-lookup"><span data-stu-id="80156-146">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="80156-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="80156-148">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="80156-148">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-149">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="80156-149">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="80156-150">Zachowanie punktów odzyskiwania dla danego czasu w godzinach.</span><span class="sxs-lookup"><span data-stu-id="80156-150">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-151">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="80156-151">-ReplicaDeletion</span></span>
<span data-ttu-id="80156-152">Określa, czy maszyna wirtualna repliki ma zostać usunięta podczas wyłączania replikacji z witryny zarządzanej programu VMM do innej.</span><span class="sxs-lookup"><span data-stu-id="80156-152">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-153">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="80156-153">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="80156-154">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="80156-154">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="80156-155">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="80156-155">Valid values are:</span></span>

- <span data-ttu-id="80156-156">30</span><span class="sxs-lookup"><span data-stu-id="80156-156">30</span></span>
- <span data-ttu-id="80156-157">300</span><span class="sxs-lookup"><span data-stu-id="80156-157">300</span></span>
- <span data-ttu-id="80156-158">900</span><span class="sxs-lookup"><span data-stu-id="80156-158">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-159">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="80156-159">-ReplicationMethod</span></span>
<span data-ttu-id="80156-160">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="80156-160">Specifies the replication method.</span></span>
<span data-ttu-id="80156-161">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="80156-161">Valid values are:</span></span>

- <span data-ttu-id="80156-162">Ekran</span><span class="sxs-lookup"><span data-stu-id="80156-162">Online</span></span>
- <span data-ttu-id="80156-163">Pracy</span><span class="sxs-lookup"><span data-stu-id="80156-163">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-164">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="80156-164">-ReplicationPort</span></span>
<span data-ttu-id="80156-165">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="80156-165">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-166">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="80156-166">-ReplicationProvider</span></span>
<span data-ttu-id="80156-167">Określa dostawcę replikacji dla zasad.</span><span class="sxs-lookup"><span data-stu-id="80156-167">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-168">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="80156-168">-ReplicationStartTime</span></span>
<span data-ttu-id="80156-169">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="80156-169">Specifies the replication start time.</span></span>
<span data-ttu-id="80156-170">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="80156-170">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-171">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="80156-171">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="80156-172">Wartość progowa punktu odzyskiwania w minutach, w którym należy ostrzec.</span><span class="sxs-lookup"><span data-stu-id="80156-172">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-173">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="80156-173">-VmmToVmm</span></span>
<span data-ttu-id="80156-174">Parametr Przełącz określający zasady do replikowania między witrynami funkcji Hyper-V zarządzanych przez serwer programu VMM.</span><span class="sxs-lookup"><span data-stu-id="80156-174">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="80156-175">-VMwareToAzure</span></span>
<span data-ttu-id="80156-176">Parametr Switch określający, że tworzone zasady replikacji będą używane do replikowania maszyn wirtualnych VMware i/lub fizycznych serwerów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="80156-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-177">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80156-177">-Confirm</span></span>
<span data-ttu-id="80156-178">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80156-178">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80156-179">-WhatIf</span></span>
<span data-ttu-id="80156-180">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80156-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80156-181">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80156-181">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80156-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80156-182">CommonParameters</span></span>
<span data-ttu-id="80156-183">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80156-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80156-184">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80156-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80156-185">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80156-185">INPUTS</span></span>

### <span data-ttu-id="80156-186">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="80156-186">None</span></span>

## <span data-ttu-id="80156-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80156-187">OUTPUTS</span></span>

### <span data-ttu-id="80156-188">System. Object</span><span class="sxs-lookup"><span data-stu-id="80156-188">System.Object</span></span>

## <span data-ttu-id="80156-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80156-189">NOTES</span></span>

## <span data-ttu-id="80156-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80156-190">RELATED LINKS</span></span>

[<span data-ttu-id="80156-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="80156-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="80156-192">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="80156-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)

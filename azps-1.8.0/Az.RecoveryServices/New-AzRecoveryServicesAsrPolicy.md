---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 98031226919b143431206fd9e3b512e6c653b8a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708631"
---
# <span data-ttu-id="e1222-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e1222-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="e1222-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1222-102">SYNOPSIS</span></span>
<span data-ttu-id="e1222-103">Tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1222-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="e1222-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1222-104">SYNTAX</span></span>

### <span data-ttu-id="e1222-105">HyperVToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1222-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1222-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="e1222-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1222-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="e1222-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1222-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="e1222-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1222-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e1222-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1222-110">Opis</span><span class="sxs-lookup"><span data-stu-id="e1222-110">DESCRIPTION</span></span>
<span data-ttu-id="e1222-111">Polecenie cmdlet **New-AzRecoveryServicesAsrPolicy** tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1222-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="e1222-112">Zasady replikacji są używane do określania ustawień replikacji, takich jak częstotliwość replikacji i liczba punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e1222-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="e1222-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1222-113">EXAMPLES</span></span>

### <span data-ttu-id="e1222-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1222-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="e1222-115">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="e1222-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="e1222-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e1222-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

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

<span data-ttu-id="e1222-117">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="e1222-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="e1222-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e1222-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
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

### <span data-ttu-id="e1222-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="e1222-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="e1222-120">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="e1222-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e1222-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1222-121">PARAMETERS</span></span>

### <span data-ttu-id="e1222-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="e1222-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="e1222-123">Określa częstotliwość (w godzinach) tworzenia spójnych punktów odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1222-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="e1222-124">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="e1222-124">-Authentication</span></span>
<span data-ttu-id="e1222-125">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="e1222-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="e1222-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e1222-126">Valid values are:</span></span>

- <span data-ttu-id="e1222-127">Dyplom</span><span class="sxs-lookup"><span data-stu-id="e1222-127">Certificate</span></span>
-  <span data-ttu-id="e1222-128">Mechanizmu</span><span class="sxs-lookup"><span data-stu-id="e1222-128">Kerberos</span></span>

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

### <span data-ttu-id="e1222-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="e1222-129">-AzureToAzure</span></span>
<span data-ttu-id="e1222-130">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="e1222-130">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="e1222-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="e1222-131">-AzureToVMware</span></span>
<span data-ttu-id="e1222-132">{{Fill AzureToVMware Description}}</span><span class="sxs-lookup"><span data-stu-id="e1222-132">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="e1222-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="e1222-133">-Compression</span></span>
<span data-ttu-id="e1222-134">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="e1222-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="e1222-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1222-135">-DefaultProfile</span></span>
<span data-ttu-id="e1222-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1222-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="e1222-137">-HyperVToAzure</span></span>
<span data-ttu-id="e1222-138">Parametr Przełącz określający zasady do replikowania maszyn wirtualnych funkcji Hyper-V na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="e1222-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="e1222-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="e1222-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="e1222-140">Określa stan synchronizacji multiVm dla zasad.</span><span class="sxs-lookup"><span data-stu-id="e1222-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="e1222-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1222-141">-Name</span></span>
<span data-ttu-id="e1222-142">Określa nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="e1222-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="e1222-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="e1222-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="e1222-144">Określa punkty odzyskiwania liczb, które mają zostać zachowane.</span><span class="sxs-lookup"><span data-stu-id="e1222-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="e1222-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e1222-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e1222-146">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="e1222-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="e1222-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="e1222-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="e1222-148">Zachowanie punktów odzyskiwania dla danego czasu w godzinach.</span><span class="sxs-lookup"><span data-stu-id="e1222-148">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="e1222-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="e1222-149">-ReplicaDeletion</span></span>
<span data-ttu-id="e1222-150">Określa, czy maszyna wirtualna repliki ma zostać usunięta podczas wyłączania replikacji z witryny zarządzanej programu VMM do innej.</span><span class="sxs-lookup"><span data-stu-id="e1222-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="e1222-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="e1222-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="e1222-152">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="e1222-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="e1222-153">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e1222-153">Valid values are:</span></span>

- <span data-ttu-id="e1222-154">30</span><span class="sxs-lookup"><span data-stu-id="e1222-154">30</span></span>
- <span data-ttu-id="e1222-155">300</span><span class="sxs-lookup"><span data-stu-id="e1222-155">300</span></span>
- <span data-ttu-id="e1222-156">900</span><span class="sxs-lookup"><span data-stu-id="e1222-156">900</span></span>

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

### <span data-ttu-id="e1222-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="e1222-157">-ReplicationMethod</span></span>
<span data-ttu-id="e1222-158">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="e1222-158">Specifies the replication method.</span></span>
<span data-ttu-id="e1222-159">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e1222-159">Valid values are:</span></span>

- <span data-ttu-id="e1222-160">Ekran</span><span class="sxs-lookup"><span data-stu-id="e1222-160">Online</span></span>
- <span data-ttu-id="e1222-161">Pracy</span><span class="sxs-lookup"><span data-stu-id="e1222-161">Offline</span></span>

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

### <span data-ttu-id="e1222-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="e1222-162">-ReplicationPort</span></span>
<span data-ttu-id="e1222-163">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="e1222-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="e1222-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="e1222-164">-ReplicationProvider</span></span>
<span data-ttu-id="e1222-165">Określa dostawcę replikacji dla zasad.</span><span class="sxs-lookup"><span data-stu-id="e1222-165">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="e1222-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="e1222-166">-ReplicationStartTime</span></span>
<span data-ttu-id="e1222-167">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="e1222-167">Specifies the replication start time.</span></span>
<span data-ttu-id="e1222-168">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="e1222-168">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="e1222-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="e1222-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="e1222-170">Wartość progowa punktu odzyskiwania w minutach, w którym należy ostrzec.</span><span class="sxs-lookup"><span data-stu-id="e1222-170">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="e1222-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="e1222-171">-VmmToVmm</span></span>
<span data-ttu-id="e1222-172">Parametr Przełącz określający zasady do replikowania między witrynami funkcji Hyper-V zarządzanych przez serwer programu VMM.</span><span class="sxs-lookup"><span data-stu-id="e1222-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="e1222-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="e1222-173">-VMwareToAzure</span></span>
<span data-ttu-id="e1222-174">Parametr Switch określający, że tworzone zasady replikacji będą używane do replikowania maszyn wirtualnych VMware i/lub fizycznych serwerów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e1222-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="e1222-175">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1222-175">-Confirm</span></span>
<span data-ttu-id="e1222-176">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1222-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1222-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1222-177">-WhatIf</span></span>
<span data-ttu-id="e1222-178">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1222-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1222-179">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1222-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1222-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1222-180">CommonParameters</span></span>
<span data-ttu-id="e1222-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1222-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1222-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1222-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1222-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1222-183">INPUTS</span></span>

### <span data-ttu-id="e1222-184">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1222-184">None</span></span>

## <span data-ttu-id="e1222-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1222-185">OUTPUTS</span></span>

### <span data-ttu-id="e1222-186">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e1222-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e1222-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1222-187">NOTES</span></span>

## <span data-ttu-id="e1222-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1222-188">RELATED LINKS</span></span>

[<span data-ttu-id="e1222-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e1222-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="e1222-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e1222-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)

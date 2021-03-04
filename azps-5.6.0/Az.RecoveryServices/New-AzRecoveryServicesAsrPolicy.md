---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 3edbee06d2e4079d8c2283cc1b3af166d81450de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956746"
---
# <span data-ttu-id="21434-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="21434-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="21434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21434-102">SYNOPSIS</span></span>
<span data-ttu-id="21434-103">Tworzy zasady replikacji usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="21434-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="21434-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21434-104">SYNTAX</span></span>

### <span data-ttu-id="21434-105">HyperVToAzure (domyślne)</span><span class="sxs-lookup"><span data-stu-id="21434-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21434-106">VChatToAzure</span><span class="sxs-lookup"><span data-stu-id="21434-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21434-107">AzureToV Jaka jest</span><span class="sxs-lookup"><span data-stu-id="21434-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21434-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="21434-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21434-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="21434-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21434-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="21434-110">DESCRIPTION</span></span>
<span data-ttu-id="21434-111">Polecenie **cmdlet New-AzRecoveryServicesAsrPolicy** tworzy zasady replikacji usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="21434-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="21434-112">Zasady replikacji służą do określania ustawień replikacji, takich jak częstotliwość replikacji i liczba punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="21434-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="21434-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21434-113">EXAMPLES</span></span>

### <span data-ttu-id="21434-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21434-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="21434-115">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="21434-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="21434-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="21434-116">Example 2</span></span>
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

<span data-ttu-id="21434-117">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="21434-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="21434-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="21434-118">Example 3</span></span>
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

### <span data-ttu-id="21434-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="21434-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="21434-120">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="21434-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="21434-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21434-121">PARAMETERS</span></span>

### <span data-ttu-id="21434-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="21434-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="21434-123">Określa częstotliwość (w godzinach), przy której mają być tworzyć spójne punkty odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21434-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="21434-124">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="21434-124">-Authentication</span></span>
<span data-ttu-id="21434-125">Określa typ używanego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="21434-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="21434-126">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="21434-126">Valid values are:</span></span>

- <span data-ttu-id="21434-127">Certyfikat</span><span class="sxs-lookup"><span data-stu-id="21434-127">Certificate</span></span>
-  <span data-ttu-id="21434-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="21434-128">Kerberos</span></span>

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

### <span data-ttu-id="21434-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="21434-129">-AzureToAzure</span></span>
<span data-ttu-id="21434-130">Parametr Przełącznik określa scenariusz tworzenia zasad platformy Azure na azure.</span><span class="sxs-lookup"><span data-stu-id="21434-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

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

### <span data-ttu-id="21434-131">-AzureToV Jaka jest</span><span class="sxs-lookup"><span data-stu-id="21434-131">-AzureToVMware</span></span>
<span data-ttu-id="21434-132">Parametr przełącznika określa scenariusz tworzenia zasad azure na vMWare.</span><span class="sxs-lookup"><span data-stu-id="21434-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="21434-133">- Compression</span><span class="sxs-lookup"><span data-stu-id="21434-133">-Compression</span></span>
<span data-ttu-id="21434-134">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="21434-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="21434-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21434-135">-DefaultProfile</span></span>
<span data-ttu-id="21434-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21434-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="21434-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="21434-137">-HyperVToAzure</span></span>
<span data-ttu-id="21434-138">Parametr przełącznika w celu określenia zasad ma być używany do replikowania maszyn wirtualnych hyper-V do platformy Azure</span><span class="sxs-lookup"><span data-stu-id="21434-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="21434-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="21434-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="21434-140">Określa stan synchronizacji wieluVm dla zasad.</span><span class="sxs-lookup"><span data-stu-id="21434-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="21434-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="21434-141">-Name</span></span>
<span data-ttu-id="21434-142">Określa nazwę zasad replikacji asr.</span><span class="sxs-lookup"><span data-stu-id="21434-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="21434-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="21434-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="21434-144">Określa punkty odzyskiwania liczb, które mają być zachowywane.</span><span class="sxs-lookup"><span data-stu-id="21434-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="21434-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21434-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="21434-146">Określa identyfikator konta magazynu platformy Azure, do których chcesz zreplikować dane.</span><span class="sxs-lookup"><span data-stu-id="21434-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="21434-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="21434-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="21434-148">Zachowaj punkty odzyskiwania dla danego czasu w godzinach.</span><span class="sxs-lookup"><span data-stu-id="21434-148">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="21434-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="21434-149">-ReplicaDeletion</span></span>
<span data-ttu-id="21434-150">Określa, czy replika maszyny wirtualnej powinna zostać usunięta przy wyłączaniu replikacji z zarządzanej witryny maszyny wirtualnej do innej.</span><span class="sxs-lookup"><span data-stu-id="21434-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="21434-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="21434-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="21434-152">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="21434-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="21434-153">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="21434-153">Valid values are:</span></span>

- <span data-ttu-id="21434-154">30</span><span class="sxs-lookup"><span data-stu-id="21434-154">30</span></span>
- <span data-ttu-id="21434-155">300</span><span class="sxs-lookup"><span data-stu-id="21434-155">300</span></span>
- <span data-ttu-id="21434-156">900</span><span class="sxs-lookup"><span data-stu-id="21434-156">900</span></span>

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

### <span data-ttu-id="21434-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="21434-157">-ReplicationMethod</span></span>
<span data-ttu-id="21434-158">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="21434-158">Specifies the replication method.</span></span>
<span data-ttu-id="21434-159">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="21434-159">Valid values are:</span></span>

- <span data-ttu-id="21434-160">Online</span><span class="sxs-lookup"><span data-stu-id="21434-160">Online</span></span>
- <span data-ttu-id="21434-161">Offline</span><span class="sxs-lookup"><span data-stu-id="21434-161">Offline</span></span>

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

### <span data-ttu-id="21434-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="21434-162">-ReplicationPort</span></span>
<span data-ttu-id="21434-163">Określa port używany na replikację.</span><span class="sxs-lookup"><span data-stu-id="21434-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="21434-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="21434-164">-ReplicationProvider</span></span>
<span data-ttu-id="21434-165">Określa dostawcę replikacji dla zasad.</span><span class="sxs-lookup"><span data-stu-id="21434-165">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="21434-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="21434-166">-ReplicationStartTime</span></span>
<span data-ttu-id="21434-167">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="21434-167">Specifies the replication start time.</span></span>
<span data-ttu-id="21434-168">Nie może być późniejsza niż 24 godziny od rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="21434-168">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="21434-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="21434-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="21434-170">Wartość progowa RPO w minutach, dla których ma być ostrzegana.</span><span class="sxs-lookup"><span data-stu-id="21434-170">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="21434-171">- Maszyny wirtualneToVmm</span><span class="sxs-lookup"><span data-stu-id="21434-171">-VmmToVmm</span></span>
<span data-ttu-id="21434-172">Parametr przełącznika określający zasady ma być używany do replikowania między witrynami hyper-V zarządzanymi przez serwer maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21434-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="21434-173">-VChatToAzure</span><span class="sxs-lookup"><span data-stu-id="21434-173">-VMwareToAzure</span></span>
<span data-ttu-id="21434-174">Parametr przełącznika określający, że tworzone zasady replikacji będą używane do replikowania maszyn wirtualnych VLogu i/lub serwerów fizycznych do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21434-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="21434-175">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21434-175">-Confirm</span></span>
<span data-ttu-id="21434-176">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="21434-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21434-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21434-177">-WhatIf</span></span>
<span data-ttu-id="21434-178">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21434-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21434-179">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="21434-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21434-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21434-180">CommonParameters</span></span>
<span data-ttu-id="21434-181">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21434-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21434-182">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21434-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21434-183">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21434-183">INPUTS</span></span>

### <span data-ttu-id="21434-184">Brak</span><span class="sxs-lookup"><span data-stu-id="21434-184">None</span></span>

## <span data-ttu-id="21434-185">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21434-185">OUTPUTS</span></span>

### <span data-ttu-id="21434-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="21434-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="21434-187">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21434-187">NOTES</span></span>

## <span data-ttu-id="21434-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21434-188">RELATED LINKS</span></span>

[<span data-ttu-id="21434-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="21434-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="21434-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="21434-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)

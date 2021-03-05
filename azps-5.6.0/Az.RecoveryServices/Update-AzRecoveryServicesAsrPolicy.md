---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 2255a2397c7096ec1a7b5f45dc4fa699649b071a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005818"
---
# <span data-ttu-id="ce0ff-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ce0ff-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="ce0ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0ff-103">Aktualizuje zasady replikacji usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="ce0ff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ce0ff-104">SYNTAX</span></span>

### <span data-ttu-id="ce0ff-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ce0ff-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce0ff-106">VChatToAzure</span><span class="sxs-lookup"><span data-stu-id="ce0ff-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0ff-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="ce0ff-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce0ff-108">AzureToV Jaka jest</span><span class="sxs-lookup"><span data-stu-id="ce0ff-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0ff-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="ce0ff-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce0ff-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ce0ff-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce0ff-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="ce0ff-111">DESCRIPTION</span></span>
<span data-ttu-id="ce0ff-112">Polecenie **cmdlet Update-AzRecoveryServicesAsrPolicy** aktualizuje określone zasady replikacji usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="ce0ff-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ce0ff-113">EXAMPLES</span></span>

### <span data-ttu-id="ce0ff-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ce0ff-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="ce0ff-115">Uruchamia operację zasad replikacji aktualizacji przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ce0ff-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ce0ff-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="ce0ff-117">Uruchamia operację zasad azure aktualizacji azure na replikację przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ce0ff-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ce0ff-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="ce0ff-119">Uruchamia zasady replikacji platformy Azure Azure przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ce0ff-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce0ff-120">PARAMETERS</span></span>

### <span data-ttu-id="ce0ff-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="ce0ff-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="ce0ff-122">Określa częstotliwość (w godzinach), przy której mają być tworzyć spójne punkty odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="ce0ff-123">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="ce0ff-123">-Authentication</span></span>
<span data-ttu-id="ce0ff-124">Określa typ używanego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="ce0ff-125">-AzureToAzure</span></span>
<span data-ttu-id="ce0ff-126">Określa odzyskiwanie po awarii platformy Azure z azure.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="ce0ff-127">-AzureToV Jaka jest</span><span class="sxs-lookup"><span data-stu-id="ce0ff-127">-AzureToVMware</span></span>
<span data-ttu-id="ce0ff-128">Określa odzyskiwanie po awarii z platformy Azure do vMWare.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="ce0ff-129">- Compression</span><span class="sxs-lookup"><span data-stu-id="ce0ff-129">-Compression</span></span>
<span data-ttu-id="ce0ff-130">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0ff-131">-DefaultProfile</span></span>
<span data-ttu-id="ce0ff-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ce0ff-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="ce0ff-133">-HyperVToAzure</span></span>
<span data-ttu-id="ce0ff-134">Przełącz parametr wskazujący, że określone zasady są używane do replikowania maszyn wirtualnych hyper-V do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce0ff-135">-InputObject</span></span>
<span data-ttu-id="ce0ff-136">Obiekt wejściowy dla polecenia cmdlet: Określa obiekt zasad replikacji asr odpowiadający aktualizowanej zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="ce0ff-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="ce0ff-138">Określa stan synchronizacji wieluVm dla zasad.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="ce0ff-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="ce0ff-140">Określa punkty odzyskiwania liczb, które mają być zachowywane.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ce0ff-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="ce0ff-142">Określa identyfikator konta magazynu Platformy Azure dla miejsca docelowego replikacji.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="ce0ff-143">Używany jako konto docelowego magazynu dla replikacji, jeśli nie podano alternatywy podczas włączania replikacji przy użyciu New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="ce0ff-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="ce0ff-145">Czas (w godzinach), aby zachować punkty odzyskiwania po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="ce0ff-146">-ReplicaDeletion</span></span>
<span data-ttu-id="ce0ff-147">Określa, czy replika maszyny wirtualnej powinna zostać usunięta przy wyłączaniu replikacji z zarządzanej witryny maszyny wirtualnej do innej.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="ce0ff-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="ce0ff-149">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="ce0ff-150">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="ce0ff-150">Valid values are:</span></span>

- <span data-ttu-id="ce0ff-151">30</span><span class="sxs-lookup"><span data-stu-id="ce0ff-151">30</span></span>
- <span data-ttu-id="ce0ff-152">300</span><span class="sxs-lookup"><span data-stu-id="ce0ff-152">300</span></span>
- <span data-ttu-id="ce0ff-153">900</span><span class="sxs-lookup"><span data-stu-id="ce0ff-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="ce0ff-154">-ReplicationMethod</span></span>
<span data-ttu-id="ce0ff-155">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="ce0ff-156">-ReplicationPort</span></span>
<span data-ttu-id="ce0ff-157">Określa port używany na replikację.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="ce0ff-158">-ReplicationStartTime</span></span>
<span data-ttu-id="ce0ff-159">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-159">Specifies the replication start time.</span></span>
<span data-ttu-id="ce0ff-160">Nie może być późniejsza niż 24 godziny od rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="ce0ff-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="ce0ff-162">Wartość progowa RPO w minutach, dla których ma być ostrzegana.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-163">- Maszyny wirtualneToVmm</span><span class="sxs-lookup"><span data-stu-id="ce0ff-163">-VmmToVmm</span></span>
<span data-ttu-id="ce0ff-164">Przełącz parametr wskazujący, że określone zasady są używane do replikowania zarządzanych maszyn wirtualnych HYPER-V przez usługę VIRTUALM między dwiema witrynami hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ff-165">-VChatToAzure</span><span class="sxs-lookup"><span data-stu-id="ce0ff-165">-VMwareToAzure</span></span>
<span data-ttu-id="ce0ff-166">Przełącz parametr wskazujący, że określone zasady są używane do replikowania wirtualnych maszyn wirtualnych do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="ce0ff-167">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce0ff-167">-Confirm</span></span>
<span data-ttu-id="ce0ff-168">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0ff-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce0ff-169">-WhatIf</span></span>
<span data-ttu-id="ce0ff-170">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce0ff-171">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0ff-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0ff-172">CommonParameters</span></span>
<span data-ttu-id="ce0ff-173">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0ff-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0ff-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce0ff-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0ff-175">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce0ff-175">INPUTS</span></span>

### <span data-ttu-id="ce0ff-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="ce0ff-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="ce0ff-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce0ff-177">OUTPUTS</span></span>

### <span data-ttu-id="ce0ff-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ce0ff-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ce0ff-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ce0ff-179">NOTES</span></span>

## <span data-ttu-id="ce0ff-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce0ff-180">RELATED LINKS</span></span>

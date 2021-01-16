---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349126"
---
# <span data-ttu-id="28684-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="28684-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="28684-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28684-102">SYNOPSIS</span></span>
<span data-ttu-id="28684-103">Aktualizuje zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28684-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="28684-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28684-104">SYNTAX</span></span>

### <span data-ttu-id="28684-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="28684-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28684-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="28684-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28684-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="28684-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28684-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="28684-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28684-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="28684-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28684-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="28684-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28684-111">Opis</span><span class="sxs-lookup"><span data-stu-id="28684-111">DESCRIPTION</span></span>
<span data-ttu-id="28684-112">Polecenie cmdlet **Update-AzRecoveryServicesAsrPolicy** aktualizuje określone zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28684-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="28684-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28684-113">EXAMPLES</span></span>

### <span data-ttu-id="28684-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28684-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="28684-115">Rozpoczyna operację aktualizowania zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="28684-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="28684-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="28684-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="28684-117">Rozpoczyna operację aktualizowania zasad replikacji platformy Azure do platformy Azure przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="28684-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="28684-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="28684-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="28684-119">Uruchamia zasady replikacji usługi Azure to Azure przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="28684-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="28684-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28684-120">PARAMETERS</span></span>

### <span data-ttu-id="28684-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="28684-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="28684-122">Określa częstotliwość (w godzinach) tworzenia spójnych punktów odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="28684-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="28684-123">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="28684-123">-Authentication</span></span>
<span data-ttu-id="28684-124">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="28684-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="28684-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="28684-125">-AzureToAzure</span></span>
<span data-ttu-id="28684-126">Określa odzyskiwanie na platformie Azure po awarii.</span><span class="sxs-lookup"><span data-stu-id="28684-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="28684-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="28684-127">-AzureToVMware</span></span>
<span data-ttu-id="28684-128">Określa odzyskiwanie platformy Azure do programu vMWare po awarii.</span><span class="sxs-lookup"><span data-stu-id="28684-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="28684-129">-Compression</span><span class="sxs-lookup"><span data-stu-id="28684-129">-Compression</span></span>
<span data-ttu-id="28684-130">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="28684-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="28684-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28684-131">-DefaultProfile</span></span>
<span data-ttu-id="28684-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28684-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="28684-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="28684-133">-HyperVToAzure</span></span>
<span data-ttu-id="28684-134">Parametr Switch wskazujący, że określone zasady są używane do replikowania maszyn wirtualnych funkcji Hyper-V na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="28684-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="28684-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28684-135">-InputObject</span></span>
<span data-ttu-id="28684-136">Obiekt wejściowy polecenia cmdlet: określa obiekt zasad replikacji ASR odpowiadający zasadom replikacji, które mają zostać zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="28684-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="28684-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="28684-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="28684-138">Określa stan synchronizacji multiVm dla zasad.</span><span class="sxs-lookup"><span data-stu-id="28684-138">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="28684-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="28684-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="28684-140">Określa punkty odzyskiwania liczb, które mają zostać zachowane.</span><span class="sxs-lookup"><span data-stu-id="28684-140">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="28684-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="28684-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="28684-142">Określa identyfikator konta usługi Azure Storage dla lokalizacji docelowej replikacji.</span><span class="sxs-lookup"><span data-stu-id="28684-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="28684-143">Używane jako docelowe konto magazynu do replikacji, jeśli nie podano elementu alternatywnego podczas włączania replikacji przy użyciu polecenia cmdlet New-AzRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="28684-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="28684-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="28684-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="28684-145">Czas w godzinach na zachowanie punktów odzyskiwania po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="28684-145">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="28684-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="28684-146">-ReplicaDeletion</span></span>
<span data-ttu-id="28684-147">Określa, czy maszyna wirtualna repliki ma zostać usunięta podczas wyłączania replikacji z witryny zarządzanej programu VMM do innej.</span><span class="sxs-lookup"><span data-stu-id="28684-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="28684-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="28684-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="28684-149">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="28684-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="28684-150">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="28684-150">Valid values are:</span></span>

- <span data-ttu-id="28684-151">30</span><span class="sxs-lookup"><span data-stu-id="28684-151">30</span></span>
- <span data-ttu-id="28684-152">300</span><span class="sxs-lookup"><span data-stu-id="28684-152">300</span></span>
- <span data-ttu-id="28684-153">900</span><span class="sxs-lookup"><span data-stu-id="28684-153">900</span></span>

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

### <span data-ttu-id="28684-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="28684-154">-ReplicationMethod</span></span>
<span data-ttu-id="28684-155">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="28684-155">Specifies the replication method.</span></span>

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

### <span data-ttu-id="28684-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="28684-156">-ReplicationPort</span></span>
<span data-ttu-id="28684-157">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="28684-157">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="28684-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="28684-158">-ReplicationStartTime</span></span>
<span data-ttu-id="28684-159">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="28684-159">Specifies the replication start time.</span></span>
<span data-ttu-id="28684-160">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="28684-160">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="28684-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="28684-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="28684-162">Wartość progowa punktu odzyskiwania w minutach, w którym należy ostrzec.</span><span class="sxs-lookup"><span data-stu-id="28684-162">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="28684-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="28684-163">-VmmToVmm</span></span>
<span data-ttu-id="28684-164">Parametr Switch wskazujący, że określone zasady są używane do replikowania maszyn wirtualnych funkcji Hyper-V zarządzanych przez program VMM między dwiema lokacjami funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="28684-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="28684-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="28684-165">-VMwareToAzure</span></span>
<span data-ttu-id="28684-166">Parametr Switch wskazujący, że określone zasady są używane do replikowania maszyn wirtualnych VMware na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="28684-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="28684-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28684-167">-Confirm</span></span>
<span data-ttu-id="28684-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28684-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28684-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28684-169">-WhatIf</span></span>
<span data-ttu-id="28684-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28684-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28684-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28684-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28684-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28684-172">CommonParameters</span></span>
<span data-ttu-id="28684-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28684-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28684-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28684-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28684-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28684-175">INPUTS</span></span>

### <span data-ttu-id="28684-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="28684-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="28684-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28684-177">OUTPUTS</span></span>

### <span data-ttu-id="28684-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="28684-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="28684-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28684-179">NOTES</span></span>

## <span data-ttu-id="28684-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28684-180">RELATED LINKS</span></span>

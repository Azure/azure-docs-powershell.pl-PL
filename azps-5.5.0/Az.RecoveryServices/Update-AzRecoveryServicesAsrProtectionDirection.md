---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183859"
---
# <span data-ttu-id="fb9ca-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="fb9ca-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="fb9ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9ca-103">Aktualizuje kierunek replikacji dla określonego elementu chronionego replikacją lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="fb9ca-104">Służy do ponownego chronienia/odwracania replikowania elementu replikowanego lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="fb9ca-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb9ca-105">SYNTAX</span></span>

### <span data-ttu-id="fb9ca-106">ByRPIObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fb9ca-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-107">AzureToV Jaka jest</span><span class="sxs-lookup"><span data-stu-id="fb9ca-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-108">VChatToAzure</span><span class="sxs-lookup"><span data-stu-id="fb9ca-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="fb9ca-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="fb9ca-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="fb9ca-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb9ca-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="fb9ca-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="fb9ca-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb9ca-115">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb9ca-115">DESCRIPTION</span></span>
<span data-ttu-id="fb9ca-116">Polecenie cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** aktualizuje kierunek replikacji dla określonego obiektu azure site Recovery po ukończeniu operacji zatwierdzania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="fb9ca-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb9ca-117">EXAMPLES</span></span>

### <span data-ttu-id="fb9ca-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb9ca-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="fb9ca-119">Rozpocznij operację kierunku aktualizacji dla określonego planu odzyskiwania i zwraca obiekt zadania ASR używany do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="fb9ca-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fb9ca-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="fb9ca-121">Rozpocznij operację kierunku aktualizacji dla określonego elementu chronionego replikacją w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenerów ochrony i przy użyciu magazynu w pamięci podręcznej (w tym samym regionie, w którym jest maszyny wirtualnej).</span><span class="sxs-lookup"><span data-stu-id="fb9ca-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="fb9ca-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fb9ca-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="fb9ca-123">Rozpocznij operację kierunku aktualizacji dla określonego elementu chronionego replikacją w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenera ochrony i podaną konfigurację replikacji dysku.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="fb9ca-124">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="fb9ca-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="fb9ca-125">Rozpocznij operację kierunku aktualizacji dla określonego zaszyfrowanego elementu chronionego replikacją w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenera ochrony i podaną konfigurację replikacji dysku.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="fb9ca-126">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="fb9ca-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="fb9ca-127">Rozpocznij operację kierunku aktualizacji dla określonego elementu chronionego replikacją w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenera ochrony i przy użyciu magazynu pamięci podręcznej (w tym samym regionie, w którym jest maszyny wirtualnej) i grupy rozmieszczenia odległości.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="fb9ca-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb9ca-128">PARAMETERS</span></span>

### <span data-ttu-id="fb9ca-129">— Konto</span><span class="sxs-lookup"><span data-stu-id="fb9ca-129">-Account</span></span>
<span data-ttu-id="fb9ca-130">Uruchomienie jako konto w celu wypchania instalacji usługi mobilności w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="fb9ca-131">Musi znajdować się na liście kont w materiałach ASR.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="fb9ca-132">-AzureToAzure</span></span>
<span data-ttu-id="fb9ca-133">Określa odzyskiwanie po awarii platformy Azure z azure.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-133">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-134">-AzureToAzureTiaReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb9ca-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="fb9ca-135">Określa konfigurację dysku na wypadek odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-135">Specifies the disk configuration for disaster recovery.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-136">-AzureToV Jaka jest</span><span class="sxs-lookup"><span data-stu-id="fb9ca-136">-AzureToVMware</span></span>
<span data-ttu-id="fb9ca-137">Określa scenariusz przełączania platformy Azure na vMWare.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="fb9ca-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="fb9ca-138">-DataStore</span></span>
<span data-ttu-id="fb9ca-139">Magazyn danych VLogi, który ma być używany dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-139">The VMware data-store to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9ca-140">-DefaultProfile</span></span>
<span data-ttu-id="fb9ca-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fb9ca-142">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="fb9ca-142">-Direction</span></span>
<span data-ttu-id="fb9ca-143">Określa kierunek, w jakim ma zostać użyta operacja aktualizacji po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="fb9ca-144">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fb9ca-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb9ca-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="fb9ca-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="fb9ca-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="fb9ca-146">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="fb9ca-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="fb9ca-148">Określa tajny adres URL szyfrowania dysku z wersją(szyfrowanie dysku platformy Azure), który ma być używany jako odzyskiwania maszyny wirtualnej po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="fb9ca-150">Określa identyfikator tajnego magazynu szyfrowania dysku (szyfrowanie dysku platformy Azure), który ma być używany jako maszyny wirtualnej odzyskiwania po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="fb9ca-151">-HyperVToAzure</span></span>
<span data-ttu-id="fb9ca-152">Reprotect a Hyper-V virtual machine after failback.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="fb9ca-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="fb9ca-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="fb9ca-154">Określa adres URL klucza szyfrowania dysku(szyfrowanie dysku platformy Azure), który ma być używany jako dysk WIRTUALNEgo odzyskiwania po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="fb9ca-156">Określa klucz klucza szyfrowania dyskuVault ID(szyfrowanie dysku platformy Azure), który ma być używany jako maszyny wirtualnej odzyskiwania po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-157">-LogStorageAccountId</span></span>
<span data-ttu-id="fb9ca-158">Określa identyfikator konta magazynu do przechowywania dziennika replikacji maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="fb9ca-159">-MasterTarget</span></span>
<span data-ttu-id="fb9ca-160">Szczegóły głównego serwera docelowego.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-160">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="fb9ca-161">-ProcessServer</span></span>
<span data-ttu-id="fb9ca-162">Serwer procesów używany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-162">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="fb9ca-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="fb9ca-164">Mapowanie kontenera ochrony na replikację.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-164">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="fb9ca-166">Zestaw dostępności, w który należy utworzyć maszynę wirtualną podczas trybu failover</span><span class="sxs-lookup"><span data-stu-id="fb9ca-166">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="fb9ca-168">Określa identyfikator konta magazynu platformy Azure, do których chcesz zreplikować dane.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="fb9ca-170">Określa konto magazynu na potrzeby diagnostyki rozruchu dla odzyskiwania maszyny wirtualnej azure.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="fb9ca-172">Identyfikator zasobu usługi w chmurze odzyskiwania w celu trybu failover tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb9ca-173">-RecoveryPlan</span></span>
<span data-ttu-id="fb9ca-174">Określa obiekt planu odzyskiwania po stronie asr.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-174">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="fb9ca-176">Identyfikator zasobu grupy położenia odległości odzyskiwania w celu trybu failover tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="fb9ca-178">Identyfikator grupy zasobów odzyskiwania dla chronionej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-178">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb9ca-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fb9ca-180">Określa element chroniony replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-180">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-181">- RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="fb9ca-181">-RetentionVolume</span></span>
<span data-ttu-id="fb9ca-182">Wolumin przechowywania na głównym serwerze docelowym, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-182">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ca-183">- Maszyny wirtualneToVmm</span><span class="sxs-lookup"><span data-stu-id="fb9ca-183">-VmmToVmm</span></span>
<span data-ttu-id="fb9ca-184">Kierunek replikacji aktualizacji dla maszyny wirtualnej hyper-V, która jest chroniona między dwoma zarządzanymi witrynami hyper-V, jest aktualizująca kierunek replikacji.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="fb9ca-185">-VChatToAzure</span><span class="sxs-lookup"><span data-stu-id="fb9ca-185">-VMwareToAzure</span></span>
<span data-ttu-id="fb9ca-186">Zaktualizuj kierunek replikacji z V Firmware do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="fb9ca-187">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb9ca-187">-Confirm</span></span>
<span data-ttu-id="fb9ca-188">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb9ca-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb9ca-189">-WhatIf</span></span>
<span data-ttu-id="fb9ca-190">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb9ca-191">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb9ca-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9ca-192">CommonParameters</span></span>
<span data-ttu-id="fb9ca-193">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb9ca-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9ca-194">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb9ca-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9ca-195">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb9ca-195">INPUTS</span></span>

### <span data-ttu-id="fb9ca-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb9ca-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="fb9ca-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb9ca-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fb9ca-198">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb9ca-198">OUTPUTS</span></span>

### <span data-ttu-id="fb9ca-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="fb9ca-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fb9ca-200">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb9ca-200">NOTES</span></span>

## <span data-ttu-id="fb9ca-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb9ca-201">RELATED LINKS</span></span>

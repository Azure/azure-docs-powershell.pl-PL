---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 32218fdb966a17cedcb51a2838acae1ae79d9f54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052482"
---
# <span data-ttu-id="cb2d1-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="cb2d1-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="cb2d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2d1-103">Aktualizuje kierunek replikacji określonego elementu chronionego replikacji lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="cb2d1-104">Służy do ponownego zabezpieczania/odtwarzania kopii zapasowej w replikowanym elemencie lub planie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="cb2d1-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb2d1-105">SYNTAX</span></span>

### <span data-ttu-id="cb2d1-106">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cb2d1-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2d1-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="cb2d1-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb2d1-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="cb2d1-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2d1-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="cb2d1-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2d1-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="cb2d1-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2d1-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="cb2d1-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2d1-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb2d1-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2d1-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="cb2d1-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2d1-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="cb2d1-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb2d1-115">Opis</span><span class="sxs-lookup"><span data-stu-id="cb2d1-115">DESCRIPTION</span></span>
<span data-ttu-id="cb2d1-116">Polecenie cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** aktualizuje kierunek replikacji określonego obiektu odzyskiwania witryny platformy Azure po zakończeniu operacji zatwierdzania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="cb2d1-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb2d1-117">EXAMPLES</span></span>

### <span data-ttu-id="cb2d1-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb2d1-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="cb2d1-119">Uruchamianie operacji zmiany kierunku aktualizacji dla określonego planu odzyskiwania i zwraca obiekt zadania ASR służący do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="cb2d1-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cb2d1-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="cb2d1-121">Uruchamianie operacji zmiany kierunku aktualizacji dla określonego elementu chronionego replikacji w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenera ochrony i korzystanie z przestrzeni dyskowej w pamięci podręcznej (w tym samym regionie co maszyna wirtualna).</span><span class="sxs-lookup"><span data-stu-id="cb2d1-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="cb2d1-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cb2d1-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="cb2d1-123">Uruchamianie operacji zmiany kierunku aktualizacji dla określonego elementu chronionego replikacji w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenera ochrony i dostarczoną konfiguracją replikacji dysków.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="cb2d1-124">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="cb2d1-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="cb2d1-125">Uruchamianie operacji zmiany kierunku aktualizacji dla określonego chronionego elementu replikacji zaszyfrowanej w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenera ochrony i dostarczoną konfiguracją replikacji dysku.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="cb2d1-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb2d1-126">PARAMETERS</span></span>

### <span data-ttu-id="cb2d1-127">— Konto</span><span class="sxs-lookup"><span data-stu-id="cb2d1-127">-Account</span></span>
<span data-ttu-id="cb2d1-128">Konto Uruchom jako, które ma być używane do wypychania usługi mobilności w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-128">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="cb2d1-129">Musi być jednym z listy kont Uruchom jako w sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-129">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="cb2d1-130">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="cb2d1-130">-AzureToAzure</span></span>
<span data-ttu-id="cb2d1-131">Określa odzyskiwanie na platformie Azure po awarii.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-131">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="cb2d1-132">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb2d1-132">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="cb2d1-133">Określa konfigurację dysku dla odzyskiwania po awarii.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-133">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="cb2d1-134">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="cb2d1-134">-AzureToVMware</span></span>
<span data-ttu-id="cb2d1-135">Określa scenariusz przełączenia platformy Azure na vMWare.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-135">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="cb2d1-136">-Datastore</span><span class="sxs-lookup"><span data-stu-id="cb2d1-136">-DataStore</span></span>
<span data-ttu-id="cb2d1-137">Magazyn danych VMware, który ma być wykorzystywany na potrzeby vmdisk.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-137">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="cb2d1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2d1-138">-DefaultProfile</span></span>
<span data-ttu-id="cb2d1-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cb2d1-140">-Direction</span><span class="sxs-lookup"><span data-stu-id="cb2d1-140">-Direction</span></span>
<span data-ttu-id="cb2d1-141">Określa kierunek, w jakim operacja aktualizacji służy do zaksięgowania pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="cb2d1-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cb2d1-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb2d1-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="cb2d1-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="cb2d1-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="cb2d1-144">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="cb2d1-145">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="cb2d1-145">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="cb2d1-146">Określa tajny adres URL szyfrowania dysku z wersją (szyfrowanie dysków Azure), który ma być odzyskiwany po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-146">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="cb2d1-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="cb2d1-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="cb2d1-148">Określa identyfikator magazynu tajnego szyfrowania dysków (szyfrowanie dysków Azure), który ma być wykorzystywany do odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="cb2d1-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="cb2d1-149">-HyperVToAzure</span></span>
<span data-ttu-id="cb2d1-150">Ponowne chronienie maszyny wirtualnej funkcji Hyper-V po powrotu po awarii.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-150">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="cb2d1-151">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="cb2d1-151">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="cb2d1-152">Określa adres URL klucza szyfrowania dysku (szyfrowanie dysków Azure), który ma być wykorzystywany do odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-152">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="cb2d1-153">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="cb2d1-153">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="cb2d1-154">Określa identyfikator magazynu kluczy klucza szyfrowania dysku (szyfrowanie dysków Azure), który ma być wykorzystywany do odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-154">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="cb2d1-155">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cb2d1-155">-LogStorageAccountId</span></span>
<span data-ttu-id="cb2d1-156">Określa identyfikator konta magazynu w celu przechowywania dziennika replikacji maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-156">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="cb2d1-157">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="cb2d1-157">-MasterTarget</span></span>
<span data-ttu-id="cb2d1-158">Szczegóły głównego serwera docelowego.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-158">Master Target Server Details.</span></span>

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

### <span data-ttu-id="cb2d1-159">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="cb2d1-159">-ProcessServer</span></span>
<span data-ttu-id="cb2d1-160">Serwer przetwarzania, który ma być wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-160">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="cb2d1-161">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="cb2d1-161">-ProtectionContainerMapping</span></span>
<span data-ttu-id="cb2d1-162">Do replikacji containerMapping jest używana ochrona.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-162">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="cb2d1-163">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="cb2d1-163">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="cb2d1-164">Zestaw dostępności, w którym maszyna wirtualna powinna zostać utworzona po przełączeniu do trybu failover</span><span class="sxs-lookup"><span data-stu-id="cb2d1-164">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="cb2d1-165">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cb2d1-165">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="cb2d1-166">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-166">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="cb2d1-167">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cb2d1-167">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="cb2d1-168">Określa konto magazynu do diagnostyki rozruchu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-168">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="cb2d1-169">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="cb2d1-169">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="cb2d1-170">Identyfikator zasobu usługi w chmurze odzyskiwania, do której ma zostać przejdzie przejście do tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-170">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="cb2d1-171">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cb2d1-171">-RecoveryPlan</span></span>
<span data-ttu-id="cb2d1-172">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-172">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="cb2d1-173">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="cb2d1-173">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="cb2d1-174">Identyfikator resourceName odzyskiwania chronionej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-174">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="cb2d1-175">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cb2d1-175">-ReplicationProtectedItem</span></span>
<span data-ttu-id="cb2d1-176">Określa element chroniony replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-176">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="cb2d1-177">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="cb2d1-177">-RetentionVolume</span></span>
<span data-ttu-id="cb2d1-178">Wolumin przechowywania na głównym serwerze docelowym do użycia.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-178">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="cb2d1-179">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="cb2d1-179">-VmmToVmm</span></span>
<span data-ttu-id="cb2d1-180">Aktualizowanie kierunku replikacji dla maszyny wirtualnej funkcji Hyper-V, która jest chroniona między dwiema witrynami funkcji Hyper-V zarządzanych przez program VMM.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-180">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="cb2d1-181">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="cb2d1-181">-VMwareToAzure</span></span>
<span data-ttu-id="cb2d1-182">Aktualizuj kierunek replikacji z usługi VMware na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-182">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="cb2d1-183">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb2d1-183">-Confirm</span></span>
<span data-ttu-id="cb2d1-184">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2d1-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2d1-185">-WhatIf</span></span>
<span data-ttu-id="cb2d1-186">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-186">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb2d1-187">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2d1-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2d1-188">CommonParameters</span></span>
<span data-ttu-id="cb2d1-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb2d1-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2d1-190">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb2d1-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2d1-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb2d1-191">INPUTS</span></span>

### <span data-ttu-id="cb2d1-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cb2d1-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="cb2d1-193">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cb2d1-193">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="cb2d1-194">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb2d1-194">OUTPUTS</span></span>

### <span data-ttu-id="cb2d1-195">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cb2d1-195">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cb2d1-196">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb2d1-196">NOTES</span></span>

## <span data-ttu-id="cb2d1-197">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb2d1-197">RELATED LINKS</span></span>

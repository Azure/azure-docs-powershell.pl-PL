---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: f27c9daa4e1d7df5b1feb3be42ccece780d66fb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183898"
---
# <span data-ttu-id="d854c-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d854c-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="d854c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d854c-102">SYNOPSIS</span></span>
<span data-ttu-id="d854c-103">Umożliwia replikację elementu chronionego przez asr przez utworzenie elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="d854c-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="d854c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d854c-104">SYNTAX</span></span>

### <span data-ttu-id="d854c-105">EnterpriseToEnterprise (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d854c-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d854c-106">VChatToAzureWith JednakowyTyp</span><span class="sxs-lookup"><span data-stu-id="d854c-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] -DiskType <String>
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d854c-107">VChatToAzure</span><span class="sxs-lookup"><span data-stu-id="d854c-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d854c-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d854c-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d854c-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="d854c-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-UseManagedDisk <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d854c-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d854c-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d854c-111">AzureToAzureWithoutButDetails</span><span class="sxs-lookup"><span data-stu-id="d854c-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d854c-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="d854c-112">DESCRIPTION</span></span>
<span data-ttu-id="d854c-113">Polecenie **cmdlet New-AzRecoveryServicesAsrReplicationProtectedItem** tworzy nowy element chroniony replikacją.</span><span class="sxs-lookup"><span data-stu-id="d854c-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="d854c-114">To polecenie cmdlet umożliwia replikację elementu, który można chronić za pomocą funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="d854c-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="d854c-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d854c-115">EXAMPLES</span></span>

### <span data-ttu-id="d854c-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d854c-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="d854c-117">Rozpoczyna operację tworzenia elementów chronionych replikacją dla określonego elementu, który można chronić za pomocą asr, i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="d854c-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d854c-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d854c-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="d854c-119">Rozpoczyna operację tworzenia elementów chronionych replikacją dla określonego elementu, który można chronić za pomocą narzędzia ASR, i zwraca zadanie asr używane do śledzenia operacji (scenariusz z oprogramowaniem vmWare do platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="d854c-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="d854c-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d854c-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="d854c-121">Rozpoczyna operację tworzenia elementów chronionych replikacją dla określonego elementu, który można chronić za pomocą narzędzia ASR, i zwraca zadanie asr używane do śledzenia operacji (scenariusz z platformy Azure do platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="d854c-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="d854c-122">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="d854c-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="d854c-123">Rozpoczyna operację tworzenia elementów chronionych replikacją dla określonego elementu Maszyny wirtualnej i zwraca zadanie asr służące do śledzenia operacji (scenariusz z azure do platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="d854c-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="d854c-124">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="d854c-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="d854c-125">Rozpoczyna operację tworzenia elementów chronionych replikacją dla określonego elementu, który można chronić za pomocą funkcji ASR, w tym selektywnych dyskietek i zwraca zadanie asr używane do śledzenia operacji (scenariusz maszyny wirtualnej na platformę Azure) z wybranymi dyskrybowaniami.</span><span class="sxs-lookup"><span data-stu-id="d854c-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="d854c-126">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="d854c-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="d854c-127">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="d854c-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="d854c-128">Rozpoczyna operację tworzenia elementów chronionych replikacją dla określonego elementu Maszyny wirtualnej i zwraca zadanie asr służące do śledzenia operacji (scenariusz z azure do platformy Azure). W przypadku szczegółów maszyny wirtualnej trybu failover przekazanych w celu szyfrowania zostaną użyte polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d854c-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="d854c-129">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="d854c-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="d854c-130">Uruchamia operację tworzenia elementów chronionych replikacją dla maszyny wirtualnej w grupie rozmieszczenia odległość i zwraca zadanie asr służące do śledzenia operacji (scenariusz z platformy Azure do platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="d854c-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="d854c-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d854c-131">PARAMETERS</span></span>

### <span data-ttu-id="d854c-132">— Konto</span><span class="sxs-lookup"><span data-stu-id="d854c-132">-Account</span></span>
<span data-ttu-id="d854c-133">Uruchomienie jako konto, które w razie potrzeby będzie używane do wypychania instalacji usługi mobilności.</span><span class="sxs-lookup"><span data-stu-id="d854c-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="d854c-134">Musi znajdować się na liście kont w materiałach ASR.</span><span class="sxs-lookup"><span data-stu-id="d854c-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d854c-135">-AzureToAzure</span></span>
<span data-ttu-id="d854c-136">Parametr przełącznika określa tworzenie replikowanego elementu na platformie Azure do scenariusza azure.</span><span class="sxs-lookup"><span data-stu-id="d854c-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-137">-AzureToAzureTiaReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d854c-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="d854c-138">Określa konfigurację dysku używanej maszyny wirtualnej dla platformy Azure w scenariuszu odzyskiwania po awarii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d854c-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-139">— AzureVmId</span><span class="sxs-lookup"><span data-stu-id="d854c-139">-AzureVmId</span></span>
<span data-ttu-id="d854c-140">Określa identyfikator maszyny wirtualnej platformy Azure dla ochrony odzyskiwania po awarii w regionie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d854c-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d854c-141">-DefaultProfile</span></span>
<span data-ttu-id="d854c-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d854c-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d854c-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="d854c-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="d854c-144">Określa tajny adres URL szyfrowania dysku z wersją(szyfrowanie dysków platformy Azure), który ma być używany jako odzyskiwania maszyny wirtualnej po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d854c-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d854c-146">Określa identyfikator zasobu zestawu szyfrowania dysku, który ma być używany do szyfrowania zarządzanych dysków.</span><span class="sxs-lookup"><span data-stu-id="d854c-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="d854c-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="d854c-148">Określa identyfikator tajnego magazynu szyfrowania dysku (szyfrowanie dysku platformy Azure), który ma być używany jako maszyny wirtualnej odzyskiwania po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="d854c-149">-DiskType</span></span>
<span data-ttu-id="d854c-150">Określa typ zarządzanej maszyny wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d854c-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="d854c-151">-HyperVToAzure</span></span>
<span data-ttu-id="d854c-152">Parametr przełącznika określający element replikowany jest maszyną wirtualną hyper-V, która jest replikowana do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d854c-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-153">-IncludeLeniaId</span><span class="sxs-lookup"><span data-stu-id="d854c-153">-IncludeDiskId</span></span>
<span data-ttu-id="d854c-154">Lista dyskerów, które należy uwzględnić w celu replikacji.</span><span class="sxs-lookup"><span data-stu-id="d854c-154">The list of disks to include for replication.</span></span> <span data-ttu-id="d854c-155">Domyślnie uwzględniane są wszystkie dyskietki.</span><span class="sxs-lookup"><span data-stu-id="d854c-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-156">-InMageAzureV2ChatInput</span><span class="sxs-lookup"><span data-stu-id="d854c-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="d854c-157">Określa dane wejściowe konfiguracji dysku dla identyfikatora dysku vMWare w celu ochrony przed określonym elementem, który można chronić.</span><span class="sxs-lookup"><span data-stu-id="d854c-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="d854c-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="d854c-159">Określa adres URL klucza szyfrowania dysku z wersją(szyfrowanie dysku platformy Azure), który ma być używany jako odzyskiwania maszyny wirtualnej po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="d854c-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="d854c-161">Określa identyfikator klucza klucza szyfrowania dysku (szyfrowanie dysku platformy Azure), który ma być używany jako maszyny wirtualnej odzyskiwania po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d854c-162">-LogStorageAccountId</span></span>
<span data-ttu-id="d854c-163">Określa identyfikator konta magazynu w dzienniku lub pamięci podręcznej, który ma być używany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="d854c-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-164">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d854c-164">-Name</span></span>
<span data-ttu-id="d854c-165">Określa nazwę elementu chronionego replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="d854c-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="d854c-166">Nazwa musi być unikatowa w magazynie.</span><span class="sxs-lookup"><span data-stu-id="d854c-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="d854c-167">— system operacyjny</span><span class="sxs-lookup"><span data-stu-id="d854c-167">-OS</span></span>
<span data-ttu-id="d854c-168">Określa rodzinę systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d854c-168">Specifies the operating system family.</span></span>
<span data-ttu-id="d854c-169">Dopuszczalne wartości dla tego parametru to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="d854c-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-170">-OS Jednakowa Nazwa</span><span class="sxs-lookup"><span data-stu-id="d854c-170">-OSDiskName</span></span>
<span data-ttu-id="d854c-171">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d854c-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="d854c-172">-ProcessServer</span></span>
<span data-ttu-id="d854c-173">Serwer procesów, za pomocą którym można replikować ten komputer.</span><span class="sxs-lookup"><span data-stu-id="d854c-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="d854c-174">Użyj listy serwerów procesów w procesie asr odpowiadającym serwerowi konfiguracji, aby określić jeden z nich.</span><span class="sxs-lookup"><span data-stu-id="d854c-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-175">- ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d854c-175">-ProtectableItem</span></span>
<span data-ttu-id="d854c-176">Określa obiekt elementu, który można chronić przez funkcję ASR, dla którego jest włączona replikacja.</span><span class="sxs-lookup"><span data-stu-id="d854c-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d854c-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="d854c-178">Określa obiekt mapowania kontenera ochrony funkcji ASR odpowiadający zasadom replikacji, które mają być używane na replikację.</span><span class="sxs-lookup"><span data-stu-id="d854c-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="d854c-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="d854c-180">Identyfikator zestawu dostępności w celu odzyskania komputera w przypadku trybu failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="d854c-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="d854c-182">Określa strefę dostępności maszyny wirtualnej odzyskiwania po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="d854c-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="d854c-184">Identyfikator sieci wirtualnej platformy Azure w celu odzyskania komputera w przypadku trybu failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d854c-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d854c-186">Określa identyfikator konta magazynu platformy Azure, do których chcesz zreplikować dane.</span><span class="sxs-lookup"><span data-stu-id="d854c-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="d854c-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="d854c-188">Podsieci w obrębie sieci wirtualnej platformy Azure odzyskiwania, do której należy dołączyć maszynę wirtualną, która zakończyła się niepowodzeniem w przypadku trybu failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d854c-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="d854c-190">Określa konto magazynu na potrzeby diagnostyki rozruchu dla odzyskiwania maszyny wirtualnej azure.</span><span class="sxs-lookup"><span data-stu-id="d854c-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="d854c-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="d854c-192">Określa identyfikator zasobu usługi odzyskiwania w chmurze do trybu failover tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d854c-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="d854c-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="d854c-194">Określ identyfikator grupy położenia odległości używany przez maszyny wirtualnej trybu failover w docelowym regionie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d854c-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="d854c-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="d854c-196">Określa ARM grupy zasobów, w której zostanie utworzona maszyny wirtualnej w przypadku trybu failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="d854c-197">-RecoveryVmName</span></span>
<span data-ttu-id="d854c-198">Nazwa maszyny wirtualnej odzyskiwania utworzonej po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="d854c-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="d854c-199">-ReplicationGroupName</span></span>
<span data-ttu-id="d854c-200">Określa nazwę grupy replikacji, która będzie używać do tworzenia punktów odzyskiwania spójnych dla wielu maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="d854c-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="d854c-201">Domyślnie każdy element chroniony replikacją jest tworzony w grupie własnych, a punkty odzyskiwania zgodne z wieloma maszynami wirtualnej nie są generowane.</span><span class="sxs-lookup"><span data-stu-id="d854c-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="d854c-202">Użyj tej opcji tylko wtedy, gdy musisz utworzyć punkty odzyskiwania spójne dla wielu maszyn wirtualnych na różnych komputerach, chroniąc wszystkie komputery do tej samej grupy replikacji.</span><span class="sxs-lookup"><span data-stu-id="d854c-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-203">-UseManaged Jednakowy</span><span class="sxs-lookup"><span data-stu-id="d854c-203">-UseManagedDisk</span></span>
<span data-ttu-id="d854c-204">Określa, czy maszynę wirtualną platformy Azure utworzoną w ramach trybu failover należy używać zarządzanych dyskietek.</span><span class="sxs-lookup"><span data-stu-id="d854c-204">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span> <span data-ttu-id="d854c-205">Akceptuje wartość Prawda lub Fałsz.</span><span class="sxs-lookup"><span data-stu-id="d854c-205">It Accepts either True or False.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-206">- Maszyny wirtualneToVmm</span><span class="sxs-lookup"><span data-stu-id="d854c-206">-VmmToVmm</span></span>
<span data-ttu-id="d854c-207">Parametr przełącznika określający element replikowany jest maszyną wirtualną Hyper-V, która jest replikowana między zarządzanymi witrynami hyper-V usługi WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="d854c-207">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="d854c-208">-VChatToAzure</span><span class="sxs-lookup"><span data-stu-id="d854c-208">-VMwareToAzure</span></span>
<span data-ttu-id="d854c-209">Parametr przełącznika określający element replikowany jest maszyną wirtualną V Jak lub serwerem fizycznym, który będzie replikowany do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d854c-209">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-210">- WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d854c-210">-WaitForCompletion</span></span>
<span data-ttu-id="d854c-211">Określa, że polecenie cmdlet powinno czekać na ukończenie operacji przed jej zwróceniem.</span><span class="sxs-lookup"><span data-stu-id="d854c-211">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d854c-212">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d854c-212">-Confirm</span></span>
<span data-ttu-id="d854c-213">Przed rozpoczęciem operacji jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d854c-213">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="d854c-214">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d854c-214">-WhatIf</span></span>
<span data-ttu-id="d854c-215">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d854c-215">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d854c-216">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d854c-216">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d854c-217">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d854c-217">CommonParameters</span></span>
<span data-ttu-id="d854c-218">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d854c-218">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d854c-219">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d854c-219">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d854c-220">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d854c-220">INPUTS</span></span>

### <span data-ttu-id="d854c-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d854c-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="d854c-222">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d854c-222">OUTPUTS</span></span>

### <span data-ttu-id="d854c-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d854c-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d854c-224">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d854c-224">NOTES</span></span>

## <span data-ttu-id="d854c-225">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d854c-225">RELATED LINKS</span></span>

[<span data-ttu-id="d854c-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d854c-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d854c-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d854c-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d854c-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d854c-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)

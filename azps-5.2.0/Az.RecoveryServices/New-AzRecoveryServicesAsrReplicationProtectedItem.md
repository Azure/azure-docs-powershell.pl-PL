---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359564"
---
# <span data-ttu-id="02b56-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02b56-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="02b56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02b56-102">SYNOPSIS</span></span>
<span data-ttu-id="02b56-103">Umożliwia replikację elementu chronionego przed ASR przez utworzenie elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="02b56-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="02b56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02b56-104">SYNTAX</span></span>

### <span data-ttu-id="02b56-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02b56-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b56-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="02b56-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b56-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="02b56-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b56-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="02b56-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b56-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="02b56-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b56-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="02b56-110">AzureToAzure</span></span>
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

### <span data-ttu-id="02b56-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="02b56-111">AzureToAzureWithoutDiskDetails</span></span>
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

## <span data-ttu-id="02b56-112">Opis</span><span class="sxs-lookup"><span data-stu-id="02b56-112">DESCRIPTION</span></span>
<span data-ttu-id="02b56-113">Polecenie cmdlet **New-AzRecoveryServicesAsrReplicationProtectedItem** tworzy nowy element chroniony replikacji.</span><span class="sxs-lookup"><span data-stu-id="02b56-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="02b56-114">Użyj tego polecenia cmdlet, aby włączyć replikację dla elementu chronionego przed ASR.</span><span class="sxs-lookup"><span data-stu-id="02b56-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="02b56-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02b56-115">EXAMPLES</span></span>

### <span data-ttu-id="02b56-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02b56-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="02b56-117">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu do ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="02b56-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="02b56-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="02b56-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="02b56-119">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu z możliwością ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji (scenariusz vmWare to Azure).</span><span class="sxs-lookup"><span data-stu-id="02b56-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="02b56-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="02b56-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="02b56-121">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu z możliwością ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji (scenariusz platformy Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="02b56-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="02b56-122">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="02b56-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="02b56-123">Rozpoczyna operację tworzenia elementu chronionego replikacją dla określonego identyfikatora maszyny wirtualnej i zwraca zadanie ASR używane do śledzenia operacji (scenariusz platformy Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="02b56-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="02b56-124">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="02b56-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="02b56-125">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu chronionego przed ASR, w tym dysków selektywnych i zwraca zadanie ASR używane do śledzenia operacji (scenariusz vmWare to Azure) z wybranymi dyskami.</span><span class="sxs-lookup"><span data-stu-id="02b56-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="02b56-126">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="02b56-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="02b56-127">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="02b56-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="02b56-128">Rozpoczyna operację tworzenia elementu chronionego replikacją dla określonego identyfikatora maszyny wirtualnej i zwraca zadanie ASR używane do śledzenia operacji (scenariusz platformy Azure to Azure). Szczegółowe informacje dotyczące maszyny wirtualnej trybu failover przekazano, że zostanie użyte polecenie cmdlet szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="02b56-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="02b56-129">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="02b56-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="02b56-130">Rozpoczyna operację tworzenia elementu chronionego replikacją maszyny wirtualnej w grupie umieszczania w pobliżu i zwraca zadanie ASR używane do śledzenia operacji (scenariusz platformy Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="02b56-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="02b56-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02b56-131">PARAMETERS</span></span>

### <span data-ttu-id="02b56-132">— Konto</span><span class="sxs-lookup"><span data-stu-id="02b56-132">-Account</span></span>
<span data-ttu-id="02b56-133">Konto Uruchom jako, które ma być używane do wypychania usługi mobilności w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="02b56-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="02b56-134">Musi być jednym z listy kont Uruchom jako w sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="02b56-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="02b56-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="02b56-135">-AzureToAzure</span></span>
<span data-ttu-id="02b56-136">Parametr Switch określa tworzenie zreplikowanego elementu w usłudze Azure na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="02b56-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="02b56-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="02b56-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="02b56-138">Określa konfigurację dysku używaną przez maszynę wirtualną do scenariusza odzyskiwania po awarii usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="02b56-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="02b56-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="02b56-139">-AzureVmId</span></span>
<span data-ttu-id="02b56-140">Określa identyfikator maszyny wirtualnej platformy Azure dla ochrony przed odzyskiwaniem po awarii w regionie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="02b56-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="02b56-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b56-141">-DefaultProfile</span></span>
<span data-ttu-id="02b56-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02b56-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="02b56-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="02b56-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="02b56-144">Określa tajny adres URL szyfrowania dysku z wersją (szyfrowanie dysków Azure), który ma być odzyskiwany po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="02b56-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="02b56-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="02b56-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="02b56-146">Określa identyfikator zasobu zestawu szyfrowanie dysków, który ma być wykorzystywany do szyfrowania zarządzanych dysków.</span><span class="sxs-lookup"><span data-stu-id="02b56-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="02b56-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="02b56-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="02b56-148">Określa identyfikator magazynu tajnego szyfrowania dysków (szyfrowanie dysków Azure), który ma być wykorzystywany do odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="02b56-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="02b56-149">-Disktype</span><span class="sxs-lookup"><span data-stu-id="02b56-149">-DiskType</span></span>
<span data-ttu-id="02b56-150">Określa typ dysku zarządzanego przez maszynę wirtualną odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="02b56-150">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="02b56-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="02b56-151">-HyperVToAzure</span></span>
<span data-ttu-id="02b56-152">Parametr Switch umożliwiający określenie replikowanego elementu jest maszyną wirtualną funkcji Hyper-V, która jest replikowana na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="02b56-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="02b56-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="02b56-153">-IncludeDiskId</span></span>
<span data-ttu-id="02b56-154">Lista dysków do uwzględnienia w replikacji.</span><span class="sxs-lookup"><span data-stu-id="02b56-154">The list of disks to include for replication.</span></span> <span data-ttu-id="02b56-155">Domyślnie wszystkie dyski są uwzględniane.</span><span class="sxs-lookup"><span data-stu-id="02b56-155">By default all disks are included.</span></span>

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

### <span data-ttu-id="02b56-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="02b56-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="02b56-157">Określa wejście konfiguracji dysku dla identyfikatora dysku programu vMWare w celu ochrony przed określonym elementem chronionym.</span><span class="sxs-lookup"><span data-stu-id="02b56-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="02b56-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="02b56-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="02b56-159">Określa adres URL klucza szyfrowania dysku z wersją (szyfrowanie dysków Azure), który ma być odzyskiwany po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="02b56-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="02b56-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="02b56-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="02b56-161">Określa klucz klucza szyfrowania dysku — identyfikator magazynu (szyfrowanie dysków Azure), który ma być wykorzystywany do odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="02b56-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="02b56-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="02b56-162">-LogStorageAccountId</span></span>
<span data-ttu-id="02b56-163">Określa identyfikator konta dziennika lub pamięci podręcznej, który ma być wykorzystywany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="02b56-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="02b56-164">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02b56-164">-Name</span></span>
<span data-ttu-id="02b56-165">Określa nazwę elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="02b56-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="02b56-166">Nazwa musi być unikatowa w obrębie magazynu.</span><span class="sxs-lookup"><span data-stu-id="02b56-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="02b56-167">-OS</span><span class="sxs-lookup"><span data-stu-id="02b56-167">-OS</span></span>
<span data-ttu-id="02b56-168">Określa rodzinę systemów operacyjnych.</span><span class="sxs-lookup"><span data-stu-id="02b56-168">Specifies the operating system family.</span></span>
<span data-ttu-id="02b56-169">Dopuszczalne wartości tego parametru to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="02b56-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="02b56-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="02b56-170">-OSDiskName</span></span>
<span data-ttu-id="02b56-171">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="02b56-171">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="02b56-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="02b56-172">-ProcessServer</span></span>
<span data-ttu-id="02b56-173">Serwer przetwarzania, który ma być używany do replikowania tego komputera.</span><span class="sxs-lookup"><span data-stu-id="02b56-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="02b56-174">Użyj listy serwerów procesów w sieci szkieletowej ASR odpowiadającej serwerowi konfiguracji, aby go określić.</span><span class="sxs-lookup"><span data-stu-id="02b56-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="02b56-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="02b56-175">-ProtectableItem</span></span>
<span data-ttu-id="02b56-176">Określa obiekt elementu umożliwiającego ochronę przed ASR, dla którego jest włączana replikacja.</span><span class="sxs-lookup"><span data-stu-id="02b56-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="02b56-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="02b56-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="02b56-178">Określa obiekt mapowania kontenera ochrony przed Autoodzyskiwaniem odpowiadający zasadom replikacji, które mają być używane do replikacji.</span><span class="sxs-lookup"><span data-stu-id="02b56-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="02b56-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="02b56-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="02b56-180">Identyfikator AvailabilitySet, do którego ma zostać odzyskana maszyna, w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="02b56-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="02b56-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="02b56-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="02b56-182">Określa strefę dostępności odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="02b56-182">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="02b56-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="02b56-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="02b56-184">Identyfikator sieci wirtualnej platformy Azure, w której należy odzyskać maszynę w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="02b56-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="02b56-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="02b56-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="02b56-186">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="02b56-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="02b56-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="02b56-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="02b56-188">Podsieć w sieci wirtualnej platformy Azure, do której ma zostać dołączona maszyna wirtualna, której dotyczy awaria, w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="02b56-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="02b56-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="02b56-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="02b56-190">Określa konto magazynu do diagnostyki rozruchu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="02b56-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="02b56-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="02b56-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="02b56-192">Określa identyfikator zasobu usługi w chmurze odzyskiwania, do której ma zostać przełączena ta maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="02b56-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="02b56-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="02b56-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="02b56-194">Określ identyfikator grupy rozmieszczenia bliskości używanej przez maszynę wirtualną trybu failover w docelowym regionie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="02b56-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

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

### <span data-ttu-id="02b56-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="02b56-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="02b56-196">Określa identyfikator ARM grupy zasobów, w której maszyna wirtualna zostanie utworzona w przypadku przełączenia w tryb pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="02b56-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="02b56-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="02b56-197">-RecoveryVmName</span></span>
<span data-ttu-id="02b56-198">Nazwa maszyny wirtualnej odzyskiwania utworzonej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="02b56-198">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="02b56-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="02b56-199">-ReplicationGroupName</span></span>
<span data-ttu-id="02b56-200">Określa nazwę grupy replikacji, która ma być używana do tworzenia spójnych punktów odzyskiwania wielu maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="02b56-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="02b56-201">Domyślnie poszczególne elementy chronione replikacji są tworzone w grupie swoich własnych i spójnych punktów odzyskiwania wielu maszyn wirtualnych nie są generowane.</span><span class="sxs-lookup"><span data-stu-id="02b56-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="02b56-202">Tej opcji należy używać tylko wtedy, gdy trzeba tworzyć wielomaszynowe spójne punkty odzyskiwania w grupie komputerów, chroniąc wszystkie komputery w tej samej grupie replikacji.</span><span class="sxs-lookup"><span data-stu-id="02b56-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="02b56-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="02b56-203">-VmmToVmm</span></span>
<span data-ttu-id="02b56-204">Parametr Przełącz określający replikowany element to maszyna wirtualna Hyper-V, która jest replikowana między zarządzanymi witrynami funkcji Hyper-V programu VMM.</span><span class="sxs-lookup"><span data-stu-id="02b56-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="02b56-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="02b56-205">-VMwareToAzure</span></span>
<span data-ttu-id="02b56-206">Parametr Switch określający replikowany element to maszyna wirtualna lub serwer fizyczny VMware, które zostaną zreplikowane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="02b56-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="02b56-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="02b56-207">-WaitForCompletion</span></span>
<span data-ttu-id="02b56-208">Określa, że polecenie cmdlet powinno czekać na ukończenie operacji przed zwróceniem.</span><span class="sxs-lookup"><span data-stu-id="02b56-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="02b56-209">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02b56-209">-Confirm</span></span>
<span data-ttu-id="02b56-210">Monituje o potwierdzenie przed rozpoczęciem operacji.</span><span class="sxs-lookup"><span data-stu-id="02b56-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="02b56-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b56-211">-WhatIf</span></span>
<span data-ttu-id="02b56-212">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02b56-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b56-213">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02b56-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02b56-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b56-214">CommonParameters</span></span>
<span data-ttu-id="02b56-215">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b56-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b56-216">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02b56-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b56-217">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02b56-217">INPUTS</span></span>

### <span data-ttu-id="02b56-218">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="02b56-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="02b56-219">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02b56-219">OUTPUTS</span></span>

### <span data-ttu-id="02b56-220">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="02b56-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="02b56-221">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02b56-221">NOTES</span></span>

## <span data-ttu-id="02b56-222">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02b56-222">RELATED LINKS</span></span>

[<span data-ttu-id="02b56-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02b56-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="02b56-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02b56-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="02b56-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02b56-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)

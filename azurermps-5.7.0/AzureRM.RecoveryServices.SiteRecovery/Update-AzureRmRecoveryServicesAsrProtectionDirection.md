---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 13d1829326695e2860caf99bf002dcf5da31caac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526634"
---
# <span data-ttu-id="9c2ea-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="9c2ea-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="9c2ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2ea-103">Aktualizuje kierunek replikacji określonego elementu chronionego replikacji lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="9c2ea-104">Służy do ponownego zabezpieczania/odtwarzania kopii zapasowej w replikowanym elemencie lub planie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c2ea-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c2ea-105">SYNTAX</span></span>

### <span data-ttu-id="9c2ea-106">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9c2ea-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2ea-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="9c2ea-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c2ea-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="9c2ea-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2ea-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="9c2ea-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2ea-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="9c2ea-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2ea-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="9c2ea-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2ea-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9c2ea-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2ea-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="9c2ea-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2ea-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="9c2ea-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c2ea-115">Opis</span><span class="sxs-lookup"><span data-stu-id="9c2ea-115">DESCRIPTION</span></span>
<span data-ttu-id="9c2ea-116">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrProtectionDirection** aktualizuje kierunek replikacji określonego obiektu odzyskiwania witryny platformy Azure po zakończeniu operacji zatwierdzania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="9c2ea-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c2ea-117">EXAMPLES</span></span>

### <span data-ttu-id="9c2ea-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c2ea-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="9c2ea-119">Uruchamianie operacji zmiany kierunku aktualizacji dla określonego planu odzyskiwania i zwraca obiekt zadania ASR służący do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="9c2ea-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9c2ea-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="9c2ea-121">Uruchamianie operacji zmiany kierunku aktualizacji dla określonego elementu chronionego replikacji w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenera ochrony i korzystanie z przestrzeni dyskowej w pamięci podręcznej (w tym samym regionie co maszyna wirtualna).</span><span class="sxs-lookup"><span data-stu-id="9c2ea-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="9c2ea-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9c2ea-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="9c2ea-123">Uruchamianie operacji zmiany kierunku aktualizacji dla określonego elementu chronionego replikacji w docelowym regionie platformy Azure zdefiniowanym przez mapowanie kontenera ochrony i dostarczoną konfiguracją replikacji dysków.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="9c2ea-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c2ea-124">PARAMETERS</span></span>

### <span data-ttu-id="9c2ea-125">— Konto</span><span class="sxs-lookup"><span data-stu-id="9c2ea-125">-Account</span></span>
<span data-ttu-id="9c2ea-126">Konto Uruchom jako, które ma być używane do wypychania usługi mobilności w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="9c2ea-127">Musi być jednym z listy kont Uruchom jako w sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="9c2ea-128">-AzureToAzure</span></span>
<span data-ttu-id="9c2ea-129">Parametr Switch określający, że kierunek replikacji replikowanych maszyn wirtualnych platformy Azure jest aktualizowany między dwoma regionami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c2ea-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="9c2ea-131">Określa listę dysków maszyny wirtualnej do zreplikowania, a następnie konto pamięci podręcznej i konto magazynu odzyskiwania, które mają być używane do replikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="9c2ea-132">-AzureToVMware</span></span>
<span data-ttu-id="9c2ea-133">Aktualizowanie kierunku replikacji z platformy Azure do VMware.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-133">Update replication direction from Azure to Vmware.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c2ea-134">-Confirm</span></span>
<span data-ttu-id="9c2ea-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-136">-Datastore</span><span class="sxs-lookup"><span data-stu-id="9c2ea-136">-DataStore</span></span>
<span data-ttu-id="9c2ea-137">Magazyn danych VMware, który ma być wykorzystywany na potrzeby vmdisk.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-137">The VMware datastore to be used for the vmdisk's.</span></span>

```yaml
Type: ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2ea-138">-DefaultProfile</span></span>
<span data-ttu-id="9c2ea-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-140">-Direction</span><span class="sxs-lookup"><span data-stu-id="9c2ea-140">-Direction</span></span>
<span data-ttu-id="9c2ea-141">Określa kierunek, w jakim operacja aktualizacji służy do zaksięgowania pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="9c2ea-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9c2ea-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c2ea-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="9c2ea-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="9c2ea-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="9c2ea-144">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-145">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="9c2ea-145">-HyperVToAzure</span></span>
<span data-ttu-id="9c2ea-146">Ponowne chronienie maszyny wirtualnej funkcji Hyper-V po powrotu po awarii.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-146">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-147">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9c2ea-147">-LogStorageAccountId</span></span>
<span data-ttu-id="9c2ea-148">Określa identyfikator konta magazynu w celu przechowywania dziennika replikacji maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-148">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-149">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="9c2ea-149">-MasterTarget</span></span>
<span data-ttu-id="9c2ea-150">Szczegóły głównego serwera docelowego.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-150">Master Target Server Details.</span></span>

```yaml
Type: ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="9c2ea-151">-ProcessServer</span></span>
<span data-ttu-id="9c2ea-152">Serwer przetwarzania, który ma być wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-152">Process Server to be used for replication.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-153">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9c2ea-153">-ProtectionContainerMapping</span></span>
<span data-ttu-id="9c2ea-154">Do replikacji containerMapping jest używana ochrona.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-154">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-155">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="9c2ea-155">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="9c2ea-156">Zestaw dostępności, w którym maszyna wirtualna powinna zostać utworzona po przełączeniu do trybu failover</span><span class="sxs-lookup"><span data-stu-id="9c2ea-156">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-157">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9c2ea-157">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="9c2ea-158">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-158">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="9c2ea-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="9c2ea-160">Identyfikator zasobu usługi w chmurze odzyskiwania, do której ma zostać przejdzie przejście do tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9c2ea-161">-RecoveryPlan</span></span>
<span data-ttu-id="9c2ea-162">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-162">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="9c2ea-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="9c2ea-164">Identyfikator resourceName odzyskiwania chronionej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-164">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9c2ea-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9c2ea-166">Określa element chroniony replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-166">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="9c2ea-167">-RetentionVolume</span></span>
<span data-ttu-id="9c2ea-168">Wolumin przechowywania na głównym serwerze docelowym do użycia.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-168">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-169">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="9c2ea-169">-VMwareToAzure</span></span>
<span data-ttu-id="9c2ea-170">Aktualizuj kierunek replikacji z usługi VMware na platformę Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-170">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="9c2ea-171">-VmmToVmm</span></span>
<span data-ttu-id="9c2ea-172">Aktualizowanie kierunku replikacji dla maszyny wirtualnej funkcji Hyper-V, która jest chroniona między dwiema witrynami funkcji Hyper-V zarządzanych przez program VMM.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-172">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c2ea-173">-WhatIf</span></span>
<span data-ttu-id="9c2ea-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c2ea-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ea-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2ea-176">CommonParameters</span></span>
<span data-ttu-id="9c2ea-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c2ea-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2ea-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c2ea-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2ea-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c2ea-179">INPUTS</span></span>

### <span data-ttu-id="9c2ea-180">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9c2ea-180">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="9c2ea-181">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9c2ea-181">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9c2ea-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c2ea-182">OUTPUTS</span></span>

### <span data-ttu-id="9c2ea-183">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9c2ea-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9c2ea-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c2ea-184">NOTES</span></span>

## <span data-ttu-id="9c2ea-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c2ea-185">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: c3c420e29d0aba3f8e64e8b5528b62dddf974984
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886690"
---
# <span data-ttu-id="71484-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71484-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="71484-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71484-102">SYNOPSIS</span></span>
<span data-ttu-id="71484-103">Umożliwia replikację elementu chronionego przed ASR przez utworzenie elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="71484-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="71484-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71484-104">SYNTAX</span></span>

### <span data-ttu-id="71484-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="71484-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71484-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="71484-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71484-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="71484-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71484-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="71484-108">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71484-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="71484-109">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71484-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="71484-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71484-111">Opis</span><span class="sxs-lookup"><span data-stu-id="71484-111">DESCRIPTION</span></span>
<span data-ttu-id="71484-112">Polecenie cmdlet **New-AzRecoveryServicesAsrReplicationProtectedItem** tworzy nowy element chroniony replikacji.</span><span class="sxs-lookup"><span data-stu-id="71484-112">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="71484-113">Użyj tego polecenia cmdlet, aby włączyć replikację dla elementu chronionego przed ASR.</span><span class="sxs-lookup"><span data-stu-id="71484-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="71484-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71484-114">EXAMPLES</span></span>

### <span data-ttu-id="71484-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71484-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="71484-116">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu do ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="71484-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="71484-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="71484-117">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="71484-118">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu z możliwością ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji (scenariusz vmWare to Azure).</span><span class="sxs-lookup"><span data-stu-id="71484-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="71484-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="71484-119">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzToAzure -AzToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="71484-120">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu z możliwością ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji (scenariusz platformy Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="71484-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="71484-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="71484-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="71484-122">Rozpoczyna operację tworzenia elementu chronionego replikacją dla określonego identyfikatora maszyny wirtualnej i zwraca zadanie ASR używane do śledzenia operacji (scenariusz platformy Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="71484-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="71484-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71484-123">PARAMETERS</span></span>

### <span data-ttu-id="71484-124">— Konto</span><span class="sxs-lookup"><span data-stu-id="71484-124">-Account</span></span>
<span data-ttu-id="71484-125">Konto Uruchom jako, które ma być używane do wypychania usługi mobilności w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="71484-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="71484-126">Musi być jednym z listy kont Uruchom jako w sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="71484-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="71484-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="71484-127">-AzureToAzure</span></span>
<span data-ttu-id="71484-128">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="71484-128">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="71484-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="71484-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="71484-130">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="71484-130">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

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

### <span data-ttu-id="71484-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="71484-131">-AzureVmId</span></span>
<span data-ttu-id="71484-132">{{Fill AzureVmId Description}}</span><span class="sxs-lookup"><span data-stu-id="71484-132">{{Fill AzureVmId Description}}</span></span>

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

### <span data-ttu-id="71484-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71484-133">-DefaultProfile</span></span>
<span data-ttu-id="71484-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71484-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="71484-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="71484-135">-HyperVToAzure</span></span>
<span data-ttu-id="71484-136">Parametr Switch umożliwiający określenie replikowanego elementu jest maszyną wirtualną funkcji Hyper-V, która jest replikowana na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="71484-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="71484-137">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="71484-137">-IncludeDiskId</span></span>
<span data-ttu-id="71484-138">Lista dysków do uwzględnienia w replikacji.</span><span class="sxs-lookup"><span data-stu-id="71484-138">The list of disks to include for replication.</span></span> <span data-ttu-id="71484-139">Domyślnie wszystkie dyski są uwzględniane.</span><span class="sxs-lookup"><span data-stu-id="71484-139">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71484-140">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="71484-140">-LogStorageAccountId</span></span>
<span data-ttu-id="71484-141">Określa identyfikator konta dziennika lub pamięci podręcznej, który ma być wykorzystywany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="71484-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="71484-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71484-142">-Name</span></span>
<span data-ttu-id="71484-143">Określa nazwę elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="71484-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="71484-144">Nazwa musi być unikatowa w obrębie magazynu.</span><span class="sxs-lookup"><span data-stu-id="71484-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="71484-145">-OS</span><span class="sxs-lookup"><span data-stu-id="71484-145">-OS</span></span>
<span data-ttu-id="71484-146">Określa rodzinę systemów operacyjnych.</span><span class="sxs-lookup"><span data-stu-id="71484-146">Specifies the operating system family.</span></span>
<span data-ttu-id="71484-147">Dopuszczalne wartości tego parametru to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="71484-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="71484-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="71484-148">-OSDiskName</span></span>
<span data-ttu-id="71484-149">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="71484-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="71484-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="71484-150">-ProcessServer</span></span>
<span data-ttu-id="71484-151">Serwer przetwarzania, który ma być używany do replikowania tego komputera.</span><span class="sxs-lookup"><span data-stu-id="71484-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="71484-152">Użyj listy serwerów procesów w sieci szkieletowej ASR odpowiadającej serwerowi konfiguracji, aby go określić.</span><span class="sxs-lookup"><span data-stu-id="71484-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71484-153">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="71484-153">-ProtectableItem</span></span>
<span data-ttu-id="71484-154">Określa obiekt elementu umożliwiającego ochronę przed ASR, dla którego jest włączana replikacja.</span><span class="sxs-lookup"><span data-stu-id="71484-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71484-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="71484-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="71484-156">Określa obiekt mapowania kontenera ochrony przed Autoodzyskiwaniem odpowiadający zasadom replikacji, które mają być używane do replikacji.</span><span class="sxs-lookup"><span data-stu-id="71484-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="71484-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="71484-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="71484-158">Identyfikator AvailabilitySet, do którego ma zostać odzyskana maszyna, w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="71484-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="71484-159">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="71484-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="71484-160">Identyfikator sieci wirtualnej platformy Azure, w której należy odzyskać maszynę w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="71484-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71484-161">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="71484-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="71484-162">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="71484-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="71484-163">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="71484-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="71484-164">Podsieć w sieci wirtualnej platformy Azure, do której ma zostać dołączona maszyna wirtualna, której dotyczy awaria, w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="71484-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71484-165">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="71484-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="71484-166">Określa konto magazynu do diagnostyki rozruchu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71484-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="71484-167">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="71484-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="71484-168">Określa identyfikator zasobu usługi w chmurze odzyskiwania, do której ma zostać przełączena ta maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="71484-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="71484-169">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="71484-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="71484-170">Określa identyfikator ARM grupy zasobów, w której maszyna wirtualna zostanie utworzona w przypadku przełączenia w tryb pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="71484-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71484-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="71484-171">-RecoveryVmName</span></span>
<span data-ttu-id="71484-172">Nazwa maszyny wirtualnej odzyskiwania utworzonej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="71484-172">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71484-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="71484-173">-ReplicationGroupName</span></span>
<span data-ttu-id="71484-174">Określa nazwę grupy replikacji, która ma być używana do tworzenia spójnych punktów odzyskiwania wielu maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="71484-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="71484-175">Domyślnie poszczególne elementy chronione replikacji są tworzone w grupie swoich własnych i spójnych punktów odzyskiwania wielu maszyn wirtualnych nie są generowane.</span><span class="sxs-lookup"><span data-stu-id="71484-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="71484-176">Tej opcji należy używać tylko wtedy, gdy trzeba tworzyć wielomaszynowe spójne punkty odzyskiwania w grupie komputerów, chroniąc wszystkie komputery w tej samej grupie replikacji.</span><span class="sxs-lookup"><span data-stu-id="71484-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71484-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="71484-177">-VmmToVmm</span></span>
<span data-ttu-id="71484-178">Parametr Przełącz określający replikowany element to maszyna wirtualna Hyper-V, która jest replikowana między zarządzanymi witrynami funkcji Hyper-V programu VMM.</span><span class="sxs-lookup"><span data-stu-id="71484-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="71484-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="71484-179">-VMwareToAzure</span></span>
<span data-ttu-id="71484-180">Parametr Switch określający replikowany element to maszyna wirtualna lub serwer fizyczny VMware, które zostaną zreplikowane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="71484-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="71484-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="71484-181">-WaitForCompletion</span></span>
<span data-ttu-id="71484-182">Określa, że polecenie cmdlet powinno czekać na ukończenie operacji przed zwróceniem.</span><span class="sxs-lookup"><span data-stu-id="71484-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="71484-183">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71484-183">-Confirm</span></span>
<span data-ttu-id="71484-184">Monituje o potwierdzenie przed rozpoczęciem operacji.</span><span class="sxs-lookup"><span data-stu-id="71484-184">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="71484-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71484-185">-WhatIf</span></span>
<span data-ttu-id="71484-186">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71484-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71484-187">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="71484-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71484-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71484-188">CommonParameters</span></span>
<span data-ttu-id="71484-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71484-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71484-190">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71484-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71484-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71484-191">INPUTS</span></span>

### <span data-ttu-id="71484-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="71484-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="71484-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71484-193">OUTPUTS</span></span>

### <span data-ttu-id="71484-194">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="71484-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71484-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71484-195">NOTES</span></span>

## <span data-ttu-id="71484-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71484-196">RELATED LINKS</span></span>

[<span data-ttu-id="71484-197">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71484-197">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="71484-198">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71484-198">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="71484-199">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="71484-199">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)

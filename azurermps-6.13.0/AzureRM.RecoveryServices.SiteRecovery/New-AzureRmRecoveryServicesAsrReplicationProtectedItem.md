---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 6a35620b7a4d8952b10973f181c2ab50f5d958b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524310"
---
# <span data-ttu-id="2e486-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2e486-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="2e486-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e486-102">SYNOPSIS</span></span>
<span data-ttu-id="2e486-103">Umożliwia replikację elementu chronionego przed ASR przez utworzenie elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="2e486-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e486-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e486-104">SYNTAX</span></span>

### <span data-ttu-id="2e486-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e486-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e486-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="2e486-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e486-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="2e486-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e486-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="2e486-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e486-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2e486-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e486-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="2e486-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e486-111">Opis</span><span class="sxs-lookup"><span data-stu-id="2e486-111">DESCRIPTION</span></span>
<span data-ttu-id="2e486-112">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** tworzy nowy element chroniony replikacji.</span><span class="sxs-lookup"><span data-stu-id="2e486-112">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="2e486-113">Użyj tego polecenia cmdlet, aby włączyć replikację dla elementu chronionego przed ASR.</span><span class="sxs-lookup"><span data-stu-id="2e486-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="2e486-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e486-114">EXAMPLES</span></span>

### <span data-ttu-id="2e486-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e486-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="2e486-116">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu do ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="2e486-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2e486-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2e486-117">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="2e486-118">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu z możliwością ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji (scenariusz vmWare to Azure).</span><span class="sxs-lookup"><span data-stu-id="2e486-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="2e486-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2e486-119">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="2e486-120">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu z możliwością ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji (scenariusz platformy Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="2e486-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="2e486-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="2e486-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="2e486-122">Rozpoczyna operację tworzenia elementu chronionego replikacją dla określonego identyfikatora maszyny wirtualnej i zwraca zadanie ASR używane do śledzenia operacji (scenariusz platformy Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="2e486-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="2e486-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e486-123">PARAMETERS</span></span>

### <span data-ttu-id="2e486-124">— Konto</span><span class="sxs-lookup"><span data-stu-id="2e486-124">-Account</span></span>
<span data-ttu-id="2e486-125">Konto Uruchom jako, które ma być używane do wypychania usługi mobilności w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="2e486-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="2e486-126">Musi być jednym z listy kont Uruchom jako w sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="2e486-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="2e486-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2e486-127">-AzureToAzure</span></span>
<span data-ttu-id="2e486-128">Parametr Przełącz umożliwiający określenie, że replikowany element jest maszyną wirtualną platformy Azure replikowanym w regionie odzyskiwania usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="2e486-128">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

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

### <span data-ttu-id="2e486-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e486-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="2e486-130">Określa listę dysków maszyny wirtualnej do zreplikowania, a następnie konto pamięci podręcznej i konto magazynu odzyskiwania, które mają być używane do replikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="2e486-130">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="2e486-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="2e486-131">-AzureVmId</span></span>
<span data-ttu-id="2e486-132">Określa identyfikator maszyny wirtualnej platformy Azure do zreplikowania.</span><span class="sxs-lookup"><span data-stu-id="2e486-132">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="2e486-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e486-133">-DefaultProfile</span></span>
<span data-ttu-id="2e486-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e486-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e486-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="2e486-135">-HyperVToAzure</span></span>
<span data-ttu-id="2e486-136">Parametr Switch umożliwiający określenie replikowanego elementu jest maszyną wirtualną funkcji Hyper-V, która jest replikowana na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2e486-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="2e486-137">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="2e486-137">-IncludeDiskId</span></span>
<span data-ttu-id="2e486-138">Lista dysków do uwzględnienia w replikacji.</span><span class="sxs-lookup"><span data-stu-id="2e486-138">The list of disks to include for replication.</span></span> <span data-ttu-id="2e486-139">Domyślnie wszystkie dyski są uwzględniane.</span><span class="sxs-lookup"><span data-stu-id="2e486-139">By default all disks are included.</span></span>

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

### <span data-ttu-id="2e486-140">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2e486-140">-LogStorageAccountId</span></span>
<span data-ttu-id="2e486-141">Określa identyfikator konta dziennika lub pamięci podręcznej, który ma być wykorzystywany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="2e486-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="2e486-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e486-142">-Name</span></span>
<span data-ttu-id="2e486-143">Określa nazwę elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="2e486-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="2e486-144">Nazwa musi być unikatowa w obrębie magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e486-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="2e486-145">-OS</span><span class="sxs-lookup"><span data-stu-id="2e486-145">-OS</span></span>
<span data-ttu-id="2e486-146">Określa rodzinę systemów operacyjnych.</span><span class="sxs-lookup"><span data-stu-id="2e486-146">Specifies the operating system family.</span></span>
<span data-ttu-id="2e486-147">Dopuszczalne wartości tego parametru to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="2e486-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="2e486-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="2e486-148">-OSDiskName</span></span>
<span data-ttu-id="2e486-149">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="2e486-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="2e486-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="2e486-150">-ProcessServer</span></span>
<span data-ttu-id="2e486-151">Serwer przetwarzania, który ma być używany do replikowania tego komputera.</span><span class="sxs-lookup"><span data-stu-id="2e486-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="2e486-152">Użyj listy serwerów procesów w sieci szkieletowej ASR odpowiadającej serwerowi konfiguracji, aby go określić.</span><span class="sxs-lookup"><span data-stu-id="2e486-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="2e486-153">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2e486-153">-ProtectableItem</span></span>
<span data-ttu-id="2e486-154">Określa obiekt elementu umożliwiającego ochronę przed ASR, dla którego jest włączana replikacja.</span><span class="sxs-lookup"><span data-stu-id="2e486-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="2e486-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2e486-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="2e486-156">Określa obiekt mapowania kontenera ochrony przed Autoodzyskiwaniem odpowiadający zasadom replikacji, które mają być używane do replikacji.</span><span class="sxs-lookup"><span data-stu-id="2e486-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="2e486-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="2e486-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="2e486-158">Identyfikator AvailabilitySet, do którego ma zostać odzyskana maszyna, w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="2e486-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="2e486-159">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="2e486-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="2e486-160">Identyfikator sieci wirtualnej platformy Azure, w której należy odzyskać maszynę w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="2e486-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="2e486-161">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2e486-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="2e486-162">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="2e486-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="2e486-163">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="2e486-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="2e486-164">Podsieć w sieci wirtualnej platformy Azure, do której ma zostać dołączona maszyna wirtualna, której dotyczy awaria, w przypadku pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="2e486-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="2e486-165">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2e486-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="2e486-166">Określa konto magazynu do diagnostyki rozruchu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e486-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="2e486-167">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="2e486-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="2e486-168">Określa identyfikator zasobu usługi w chmurze odzyskiwania, do której ma zostać przełączena ta maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="2e486-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="2e486-169">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="2e486-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="2e486-170">Określa identyfikator ARM grupy zasobów, w której maszyna wirtualna zostanie utworzona w przypadku przełączenia w tryb pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="2e486-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="2e486-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="2e486-171">-RecoveryVmName</span></span>
<span data-ttu-id="2e486-172">Nazwa maszyny wirtualnej odzyskiwania utworzonej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="2e486-172">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="2e486-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="2e486-173">-ReplicationGroupName</span></span>
<span data-ttu-id="2e486-174">Określa nazwę grupy replikacji, która ma być używana do tworzenia spójnych punktów odzyskiwania wielu maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="2e486-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="2e486-175">Domyślnie poszczególne elementy chronione replikacji są tworzone w grupie swoich własnych i spójnych punktów odzyskiwania wielu maszyn wirtualnych nie są generowane.</span><span class="sxs-lookup"><span data-stu-id="2e486-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="2e486-176">Tej opcji należy używać tylko wtedy, gdy trzeba tworzyć wielomaszynowe spójne punkty odzyskiwania w grupie komputerów, chroniąc wszystkie komputery w tej samej grupie replikacji.</span><span class="sxs-lookup"><span data-stu-id="2e486-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="2e486-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="2e486-177">-VmmToVmm</span></span>
<span data-ttu-id="2e486-178">Parametr Przełącz określający replikowany element to maszyna wirtualna Hyper-V, która jest replikowana między zarządzanymi witrynami funkcji Hyper-V programu VMM.</span><span class="sxs-lookup"><span data-stu-id="2e486-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="2e486-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="2e486-179">-VMwareToAzure</span></span>
<span data-ttu-id="2e486-180">Parametr Switch określający replikowany element to maszyna wirtualna lub serwer fizyczny VMware, które zostaną zreplikowane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2e486-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="2e486-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="2e486-181">-WaitForCompletion</span></span>
<span data-ttu-id="2e486-182">Określa, że polecenie cmdlet powinno czekać na ukończenie operacji przed zwróceniem.</span><span class="sxs-lookup"><span data-stu-id="2e486-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="2e486-183">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e486-183">-Confirm</span></span>
<span data-ttu-id="2e486-184">Monituje o potwierdzenie przed rozpoczęciem operacji.</span><span class="sxs-lookup"><span data-stu-id="2e486-184">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="2e486-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e486-185">-WhatIf</span></span>
<span data-ttu-id="2e486-186">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e486-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e486-187">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e486-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e486-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e486-188">CommonParameters</span></span>
<span data-ttu-id="2e486-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e486-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e486-190">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e486-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e486-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e486-191">INPUTS</span></span>

### <span data-ttu-id="2e486-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2e486-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="2e486-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e486-193">OUTPUTS</span></span>

### <span data-ttu-id="2e486-194">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2e486-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2e486-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e486-195">NOTES</span></span>

## <span data-ttu-id="2e486-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e486-196">RELATED LINKS</span></span>

[<span data-ttu-id="2e486-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2e486-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="2e486-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2e486-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="2e486-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2e486-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

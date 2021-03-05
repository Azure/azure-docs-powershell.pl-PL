---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: ad3f2c07d358819917706253df05bfd899c3b53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997459"
---
# <span data-ttu-id="abbd6-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="abbd6-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="abbd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abbd6-102">SYNOPSIS</span></span>
<span data-ttu-id="abbd6-103">Ustawia właściwości odzyskiwania, takie jak sieć docelowa i rozmiar maszyny wirtualnej dla określonego elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="abbd6-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="abbd6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="abbd6-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abbd6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="abbd6-105">DESCRIPTION</span></span>
<span data-ttu-id="abbd6-106">Polecenie cmdlet **Set-AzRecoveryServicesAsrReplicationProtectedItem** ustawia właściwości odzyskiwania elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="abbd6-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="abbd6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="abbd6-107">EXAMPLES</span></span>

### <span data-ttu-id="abbd6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="abbd6-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="abbd6-109">Rozpoczyna operację aktualizowania ustawień elementów chronionych replikacją przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="abbd6-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="abbd6-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="abbd6-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="abbd6-111">Rozpoczyna operację aktualizowania ustawień karty interfejsu sieciowego elementu chronionego replikacją (zmniejszenie NIC) przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="abbd6-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="abbd6-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="abbd6-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="abbd6-113">Rozpoczyna operację aktualizowania podstawowego elementu chronionego replikacją nic(do użycia dla odzyskanych ustawień maszyny wirtualnej) przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="abbd6-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="abbd6-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="abbd6-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="abbd6-115">Rozpoczyna operację aktualizowania ustawień elementu chronionego replikacją NIC (używanego dla odzyskanej maszyny wirtualnej) przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="abbd6-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="abbd6-116">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="abbd6-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="abbd6-117">Rozpoczyna operację aktualizowania elementu chronionego replikacją wybranego elementu noc noc włączyć przyspieszone sieci przy odzyskiwaniu maszyny WIRTUALNEj (dla platformy Azure do odzyskiwania po awarii platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="abbd6-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="abbd6-118">Nie pass -EnableAcceleratedNetworkingOnRecovery, aby wyłączyć przyspieszone sieci.</span><span class="sxs-lookup"><span data-stu-id="abbd6-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="abbd6-119">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="abbd6-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="abbd6-120">Rozpocznij operację aktualizacji dla określonego zaszyfrowanego elementu chronionego replikacją, aby użyć podanych szczegółów szyfrowania dla maszyny wirtualnej trybu failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="abbd6-121">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="abbd6-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="abbd6-122">Uruchom operację aktualizacji dla określonego elementu chronionego replikacją, aby użyć podanej grupy położenia odległości dla maszyny wirtualnej trybu failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="abbd6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abbd6-123">PARAMETERS</span></span>

### <span data-ttu-id="abbd6-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="abbd6-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="abbd6-125">Określa szczegóły konfiguracji testów trybu failover i nic trybu failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-125">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="abbd6-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="abbd6-127">Określa konfigurację dysku do upated dla zarządzanej maszyny wirtualnej dysku (Azure to Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="abbd6-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abbd6-128">-DefaultProfile</span></span>
<span data-ttu-id="abbd6-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="abbd6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="abbd6-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="abbd6-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="abbd6-131">Określa tajny adres URL szyfrowania dysku z wersją(szyfrowanie dysku platformy Azure), który ma być używany jako odzyskiwania maszyny wirtualnej po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="abbd6-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="abbd6-133">Określa identyfikator magazynu klucza tajnego szyfrowania dysku(szyfrowanie dysku platformy Azure), który ma być używany jako odzyskiwania maszyny wirtualnej po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-134">-DiskIdTo DefragmentEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="abbd6-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="abbd6-135">Słownik z identyfikatorem zasobu dysku ustawionym jako identyfikator ARM dysków.</span><span class="sxs-lookup"><span data-stu-id="abbd6-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="abbd6-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="abbd6-137">Określa określoną wartość NIC na maszyny wirtualnej odzyskiwania po trybie failover z przyspieszonym trybem sieci.</span><span class="sxs-lookup"><span data-stu-id="abbd6-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="abbd6-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abbd6-138">-InputObject</span></span>
<span data-ttu-id="abbd6-139">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacją asr, odpowiadający elementowi chronionego replikacją do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="abbd6-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="abbd6-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="abbd6-141">Określa wersję adresu URL klucza szyfrowania dysku (szyfrowanie dysku platformy Azure), która ma być używana jako odzyskiwania maszyny wirtualnej po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="abbd6-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="abbd6-143">Określa klucz klucza szyfrowania dyskuVault ID(szyfrowanie dysku platformy Azure), który ma być używany jako maszyny wirtualnej odzyskiwania po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="abbd6-144">-LicenseType</span></span>
<span data-ttu-id="abbd6-145">Specyfikuj wybór typu licencji, który ma być używany dla maszyn wirtualnych systemu Windows Server.</span><span class="sxs-lookup"><span data-stu-id="abbd6-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="abbd6-146">Jeśli masz prawo do używania korzyści z używania hybrydowego rozwiązania azure (HUB) do migracji i chcesz określić, że ustawienie CENTRUM ma być używane w przypadku awarii tego chronionego elementu, ustaw dla tego chronionego elementu typ licencji: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="abbd6-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-147">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="abbd6-147">-Name</span></span>
<span data-ttu-id="abbd6-148">Określa nazwę maszyny wirtualnej odzyskiwania, która zostanie utworzona w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="abbd6-149">-NicSelectionType</span></span>
<span data-ttu-id="abbd6-150">Określa właściwości karty interfejsu sieciowego (NIC) ustawiane domyślnie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="abbd6-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="abbd6-151">Aby wrócić do wartości domyślnych, możesz określić wartość NotSelected (Niesłyszące).</span><span class="sxs-lookup"><span data-stu-id="abbd6-151">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="abbd6-152">-PrimaryNic</span></span>
<span data-ttu-id="abbd6-153">Określa wartość NIC, która będzie używana jako podstawowa karta NIC dla recvcovery MASZYNY WIRTUALNEj po zakończeniu trybu failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="abbd6-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="abbd6-155">Zestaw dostępności dla elementu chronionego replikacją po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-155">Availability set for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="abbd6-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="abbd6-157">Określa strefę dostępności dla elementu chronionego replikacją po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-157">Specifies availability zone for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="abbd6-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="abbd6-159">Określa konto magazynu na potrzeby diagnostyki rozruchu dla odzyskiwania maszyny wirtualnej azure.</span><span class="sxs-lookup"><span data-stu-id="abbd6-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="abbd6-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="abbd6-161">Identyfikator zasobu usługi odzyskiwania w chmurze do trybu failover tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="abbd6-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="abbd6-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="abbd6-163">Określa pule docelowych adresów zaplecza, które mają być skojarzone z skojarzoną z siecią NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="abbd6-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="abbd6-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="abbd6-165">Określa identyfikator sieci wirtualnej platformy Azure, w której należy przelać element chroniony.</span><span class="sxs-lookup"><span data-stu-id="abbd6-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="abbd6-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="abbd6-167">Określa identyfikator grupy zabezpieczeń sieci, która ma zostać skojarzona z skojarzoną z siecią NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="abbd6-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-168">-RecoveryNicDressIPAddress</span><span class="sxs-lookup"><span data-stu-id="abbd6-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="abbd6-169">Określa statyczny adres IP, który powinien być przypisany do podstawowej karty NIC podczas odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="abbd6-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="abbd6-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="abbd6-171">Określa nazwę podsieci w wirtualnej sieci azure odzyskiwania, z którą ten element chroniony powinien być połączony w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="abbd6-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="abbd6-173">Określa identyfikator zasobu grupy położenia odległości odzyskiwania do trybu failover maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="abbd6-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="abbd6-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="abbd6-175">Określa identyfikator publicznego zasobu adresu IP, który ma zostać skojarzony z skojarzoną z skojarzoną z siecią NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="abbd6-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="abbd6-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="abbd6-177">Identyfikator grupy zasobów platformy Azure w regionie odzyskiwania, w którym chroniony element zostanie odzyskany w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-178">— Rozmiar</span><span class="sxs-lookup"><span data-stu-id="abbd6-178">-Size</span></span>
<span data-ttu-id="abbd6-179">Określa rozmiar maszyny wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="abbd6-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="abbd6-180">Wartość powinna pochodzić z zestawu rozmiarów obsługiwanych przez maszyny wirtualne platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="abbd6-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-181">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="abbd6-181">-TfoAzureVMName</span></span>
<span data-ttu-id="abbd6-182">Określa nazwę testowej maszyny wirtualnej trybu failover.</span><span class="sxs-lookup"><span data-stu-id="abbd6-182">Specifies the name of the test failover VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="abbd6-183">-UpdateNic</span></span>
<span data-ttu-id="abbd6-184">Określa wartość NIC maszyny wirtualnej, dla której to polecenie cmdlet ustawia właściwość sieci odzyskiwania wymaga udpated.</span><span class="sxs-lookup"><span data-stu-id="abbd6-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbd6-185">-UseManaged Jednakowy</span><span class="sxs-lookup"><span data-stu-id="abbd6-185">-UseManagedDisk</span></span>
<span data-ttu-id="abbd6-186">Określa, czy maszyną wirtualną platformy Azure utworzoną w ramach trybu failover powinny być dyskietki zarządzane.</span><span class="sxs-lookup"><span data-stu-id="abbd6-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="abbd6-187">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="abbd6-187">-Confirm</span></span>
<span data-ttu-id="abbd6-188">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="abbd6-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abbd6-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abbd6-189">-WhatIf</span></span>
<span data-ttu-id="abbd6-190">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abbd6-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abbd6-191">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="abbd6-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abbd6-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abbd6-192">CommonParameters</span></span>
<span data-ttu-id="abbd6-193">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abbd6-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abbd6-194">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abbd6-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abbd6-195">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abbd6-195">INPUTS</span></span>

### <span data-ttu-id="abbd6-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="abbd6-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="abbd6-197">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abbd6-197">OUTPUTS</span></span>

### <span data-ttu-id="abbd6-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="abbd6-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="abbd6-199">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="abbd6-199">NOTES</span></span>

## <span data-ttu-id="abbd6-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abbd6-200">RELATED LINKS</span></span>

[<span data-ttu-id="abbd6-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="abbd6-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="abbd6-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="abbd6-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="abbd6-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="abbd6-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

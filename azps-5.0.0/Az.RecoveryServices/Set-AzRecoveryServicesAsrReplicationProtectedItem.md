---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224672"
---
# <span data-ttu-id="076c6-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="076c6-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="076c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="076c6-102">SYNOPSIS</span></span>
<span data-ttu-id="076c6-103">Ustawia właściwości odzyskiwania, takie jak Sieć docelowa i rozmiar maszyny wirtualnej dla określonego elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="076c6-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="076c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="076c6-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="076c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="076c6-105">DESCRIPTION</span></span>
<span data-ttu-id="076c6-106">Polecenie cmdlet **Set-AzRecoveryServicesAsrReplicationProtectedItem** ustawia właściwości odzyskiwania elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="076c6-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="076c6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="076c6-107">EXAMPLES</span></span>

### <span data-ttu-id="076c6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="076c6-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="076c6-109">Rozpoczyna działanie aktualizowania ustawień elementu chronionego replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="076c6-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="076c6-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="076c6-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="076c6-111">Rozpoczyna działanie aktualizowania ustawień karty interfejsu sieciowego elementu chronionego replikacji (zmniejszenie karty sieciowej) przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="076c6-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="076c6-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="076c6-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="076c6-113">Umożliwia uruchomienie operacji aktualizowania podstawowej karty sieciowej elementu chronionego replikacji (używanej dla odzyskanych maszyn wirtualnych) przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="076c6-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="076c6-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="076c6-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="076c6-115">Umożliwia uruchomienie operacji aktualizowania karty sieciowej elementu chronionego replikacji (w celu użycia jej jako odzyskanej maszyny wirtualnej) przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="076c6-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="076c6-116">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="076c6-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="076c6-117">Rozpoczyna operację aktualizowania zaznaczonego elementu chronionego replikacją noc TP Włącz przyspieszanie obsługi sieci na maszynie wirtualnej odzyskiwania (na platformie odzyskiwania po awarii usługi Azure).</span><span class="sxs-lookup"><span data-stu-id="076c6-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="076c6-118">Jan EnableAcceleratedNetworkingOnRecovery, aby wyłączyć przyspieszone połączenia sieciowe.</span><span class="sxs-lookup"><span data-stu-id="076c6-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="076c6-119">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="076c6-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="076c6-120">Rozpocznij operację aktualizowania określonego elementu chronionego replikacji szyfrowana, aby użyć dostarczonych szczegółów szyfrowania dla maszyny wirtualnej trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="076c6-121">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="076c6-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="076c6-122">Rozpocznij operację aktualizowania określonego elementu chronionego replikacji, aby użyć udostępnionej grupy położenia usługi zbliżeniowej dla maszyny wirtualnej trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>


## <span data-ttu-id="076c6-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="076c6-123">PARAMETERS</span></span>

### <span data-ttu-id="076c6-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="076c6-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="076c6-125">Określa szczegóły konfiguracji karty interfejsu sieciowego trybu failover i pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="076c6-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="076c6-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="076c6-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="076c6-127">Określa konfigurację dysku do udpated dla zarządzanych maszyn wirtualnych (Azure to Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="076c6-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="076c6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076c6-128">-DefaultProfile</span></span>
<span data-ttu-id="076c6-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="076c6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="076c6-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="076c6-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="076c6-131">Określa tajny adres URL szyfrowania dysku z wersją (szyfrowanie dysków Azure), który ma być odzyskiwany po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="076c6-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="076c6-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="076c6-133">Określa identyfikator magazynu kluczy tajnych szyfrowania dysków (szyfrowanie dysków Azure), który ma być wykorzystywany do odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="076c6-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="076c6-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="076c6-135">Słownik identyfikatora zasobu dysku na szyfrowanie dysków ustaw identyfikator ARM.</span><span class="sxs-lookup"><span data-stu-id="076c6-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="076c6-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="076c6-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="076c6-137">Określa określoną kartę sieciową w maszynie odzyskiwania po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="076c6-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="076c6-138">-InputObject</span></span>
<span data-ttu-id="076c6-139">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej replikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="076c6-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="076c6-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="076c6-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="076c6-141">Określa wersję adresu URL klucza szyfrowania dysku (szyfrowanie dysków Azure), która ma być używana do odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="076c6-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="076c6-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="076c6-143">Określa identyfikator magazynu kluczy klucza szyfrowania dysku (szyfrowanie dysków Azure), który ma być wykorzystywany do odzyskiwania maszyny wirtualnej po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="076c6-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="076c6-144">-LicenseType</span></span>
<span data-ttu-id="076c6-145">Określ typ licencji, który ma być wykorzystywany na potrzeby maszyn wirtualnych systemu Windows Server.</span><span class="sxs-lookup"><span data-stu-id="076c6-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="076c6-146">Jeśli masz prawo do korzystania z funkcji korzystania z usługi Azure hybrydowego (KONCENTRATORa) do migracji, a chcesz określić, że ustawienie KONCENTRATORa ma być używane podczas nieprzekraczania tego chronionego elementu, ustaw typ licencji na WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="076c6-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="076c6-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="076c6-147">-Name</span></span>
<span data-ttu-id="076c6-148">Określa nazwę maszyny wirtualnej odzyskiwania, która zostanie utworzona w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="076c6-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="076c6-149">-NicSelectionType</span></span>
<span data-ttu-id="076c6-150">Określa właściwości karty interfejsu sieciowego (NIC), które są ustawiane przez użytkownika lub ustawione domyślnie.</span><span class="sxs-lookup"><span data-stu-id="076c6-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="076c6-151">Możesz określić NotSelected, aby wrócić do wartości domyślnych.</span><span class="sxs-lookup"><span data-stu-id="076c6-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="076c6-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="076c6-152">-PrimaryNic</span></span>
<span data-ttu-id="076c6-153">Określa kartę interfejsu sieciowego, która będzie używana jako podstawowa karta sieciowa dla maszyny wirtualnej recvcovery po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="076c6-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="076c6-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="076c6-155">Zestaw dostępności dla elementu chronionego replikacji po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="076c6-156">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="076c6-156">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="076c6-157">Określa konto magazynu do diagnostyki rozruchu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="076c6-157">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="076c6-158">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="076c6-158">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="076c6-159">Identyfikator zasobu usługi w chmurze odzyskiwania, do której ma zostać przejdzie przejście do tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="076c6-159">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="076c6-160">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="076c6-160">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="076c6-161">Określa pule adresów docelowej bazy danych, które mają być skojarzone z kartą sieciową odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="076c6-161">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="076c6-162">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="076c6-162">-RecoveryNetworkId</span></span>
<span data-ttu-id="076c6-163">Określa identyfikator sieci wirtualnej platformy Azure, do której należy przejść w celu przekroczenia ochrony elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="076c6-163">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="076c6-164">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="076c6-164">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="076c6-165">Określa identyfikator grupy zabezpieczeń sieci, która ma być skojarzona z kartą sieciową odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="076c6-165">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="076c6-166">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="076c6-166">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="076c6-167">Określa statyczny adres IP, który powinien być przypisany do podstawowej karty sieciowej przy odzyskiwaniu.</span><span class="sxs-lookup"><span data-stu-id="076c6-167">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="076c6-168">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="076c6-168">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="076c6-169">Określa nazwę podsieci w wirtualnej sieci Azure, do której ma być podłączona ta karta sieciowa chronionego elementu w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-169">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="076c6-170">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="076c6-170">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="076c6-171">Określa identyfikator zasobu grupy lokalizacja zbliżeniowe odzyskiwania w celu przejścia do trybu failover maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="076c6-171">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="076c6-172">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="076c6-172">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="076c6-173">Określa identyfikator publicznego zasobu adresu IP, który ma być skojarzony z kartą sieciową odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="076c6-173">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="076c6-174">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="076c6-174">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="076c6-175">Identyfikator grupy zasobów platformy Azure w regionie odzyskiwania, w którym chroniony element zostanie przywrócony po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-175">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="076c6-176">-Size</span><span class="sxs-lookup"><span data-stu-id="076c6-176">-Size</span></span>
<span data-ttu-id="076c6-177">Określa rozmiar maszyny wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="076c6-177">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="076c6-178">Wartość powinna pochodzić z zestawu rozmiarów obsługiwanych przez maszyny wirtualne platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="076c6-178">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="076c6-179">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="076c6-179">-TfoAzureVMName</span></span>
<span data-ttu-id="076c6-180">Określa nazwę testowej maszyny wirtualnej w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="076c6-180">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="076c6-181">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="076c6-181">-UpdateNic</span></span>
<span data-ttu-id="076c6-182">Określa kartę sieciową maszyny wirtualnej, dla której to polecenie cmdlet ustawia właściwość sieć odzyskiwania wymaga udpated.</span><span class="sxs-lookup"><span data-stu-id="076c6-182">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="076c6-183">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="076c6-183">-UseManagedDisk</span></span>
<span data-ttu-id="076c6-184">Określa, czy maszyna wirtualna Azure utworzona w trybie failover powinna korzystać z dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="076c6-184">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="076c6-185">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="076c6-185">-Confirm</span></span>
<span data-ttu-id="076c6-186">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="076c6-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="076c6-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="076c6-187">-WhatIf</span></span>
<span data-ttu-id="076c6-188">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="076c6-188">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="076c6-189">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="076c6-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="076c6-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076c6-190">CommonParameters</span></span>
<span data-ttu-id="076c6-191">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="076c6-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076c6-192">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="076c6-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076c6-193">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="076c6-193">INPUTS</span></span>

### <span data-ttu-id="076c6-194">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="076c6-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="076c6-195">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="076c6-195">OUTPUTS</span></span>

### <span data-ttu-id="076c6-196">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="076c6-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="076c6-197">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="076c6-197">NOTES</span></span>

## <span data-ttu-id="076c6-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="076c6-198">RELATED LINKS</span></span>

[<span data-ttu-id="076c6-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="076c6-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="076c6-200">Nowe — AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="076c6-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="076c6-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="076c6-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

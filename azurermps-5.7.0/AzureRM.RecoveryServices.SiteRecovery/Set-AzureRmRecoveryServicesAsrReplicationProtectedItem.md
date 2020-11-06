---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: a3ae73e9831202418d35481270a1d04b1cb09a59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544196"
---
# <span data-ttu-id="3f2a0-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f2a0-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="3f2a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2a0-103">Ustawia właściwości odzyskiwania, takie jak Sieć docelowa i rozmiar maszyny wirtualnej dla określonego elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f2a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f2a0-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f2a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f2a0-105">DESCRIPTION</span></span>
<span data-ttu-id="3f2a0-106">Polecenie cmdlet **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** ustawia właściwości odzyskiwania elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="3f2a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f2a0-107">EXAMPLES</span></span>

### <span data-ttu-id="3f2a0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f2a0-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="3f2a0-109">Rozpoczyna operację aktualizowania ustawień elementu ochrony replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3f2a0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f2a0-110">PARAMETERS</span></span>

### <span data-ttu-id="3f2a0-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f2a0-111">-Confirm</span></span>
<span data-ttu-id="3f2a0-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f2a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2a0-113">-DefaultProfile</span></span>
<span data-ttu-id="3f2a0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="3f2a0-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3f2a0-115">-InputObject</span></span>
<span data-ttu-id="3f2a0-116">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej replikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3f2a0-117">-LicenseType</span></span>
<span data-ttu-id="3f2a0-118">Określ typ licencji, który ma być wykorzystywany na potrzeby maszyn wirtualnych systemu Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="3f2a0-119">Jeśli masz prawo do korzystania z funkcji korzystania z usługi Azure hybrydowego (KONCENTRATORa) do migracji, a chcesz określić, że ustawienie KONCENTRATORa ma być używane podczas nieprzekraczania tego chronionego elementu, ustaw typ licencji na WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f2a0-120">-Name</span></span>
<span data-ttu-id="3f2a0-121">Określa nazwę maszyny wirtualnej odzyskiwania, która zostanie utworzona w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="3f2a0-122">-NicSelectionType</span></span>
<span data-ttu-id="3f2a0-123">Określa właściwości karty interfejsu sieciowego (NIC), które są ustawiane przez użytkownika lub ustawione domyślnie.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="3f2a0-124">Możesz określić NotSelected, aby wrócić do wartości domyślnych.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="3f2a0-125">-PrimaryNic</span></span>
<span data-ttu-id="3f2a0-126">Określa kartę sieciową maszyny wirtualnej, dla której to polecenie cmdlet ustawia właściwość sieć odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3f2a0-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="3f2a0-128">Zestaw dostępności dla elementu chronionego replikacji po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-128">Availability set for replication protected item after failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-129">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="3f2a0-129">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="3f2a0-130">Identyfikator zasobu usługi w chmurze odzyskiwania, do której ma zostać przejdzie przejście do tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-130">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-131">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="3f2a0-131">-RecoveryNetworkId</span></span>
<span data-ttu-id="3f2a0-132">Określa identyfikator sieci wirtualnej platformy Azure, do której należy przejść w celu przekroczenia ochrony elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-132">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-133">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="3f2a0-133">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="3f2a0-134">Określa statyczny adres IP, który powinien być przypisany do podstawowej karty sieciowej przy odzyskiwaniu.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-134">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-135">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="3f2a0-135">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="3f2a0-136">Określa nazwę podsieci w wirtualnej sieci Azure, do której ma być podłączona ta karta sieciowa chronionego elementu w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-136">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-137">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="3f2a0-137">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="3f2a0-138">Identyfikator grupy zasobów platformy Azure w regionie odzyskiwania, w którym chroniony element zostanie przywrócony po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-138">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-139">-Size</span><span class="sxs-lookup"><span data-stu-id="3f2a0-139">-Size</span></span>
<span data-ttu-id="3f2a0-140">Określa rozmiar maszyny wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-140">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="3f2a0-141">Wartość powinna pochodzić z zestawu rozmiarów obsługiwanych przez maszyny wirtualne platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-141">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-142">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3f2a0-142">-UseManagedDisk</span></span>
<span data-ttu-id="3f2a0-143">Określa, czy maszyna wirtualna Azure utworzona w trybie failover powinna korzystać z dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-143">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f2a0-144">-WhatIf</span></span>
<span data-ttu-id="3f2a0-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f2a0-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f2a0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2a0-147">CommonParameters</span></span>
<span data-ttu-id="3f2a0-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2a0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2a0-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f2a0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2a0-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f2a0-150">INPUTS</span></span>

### <span data-ttu-id="3f2a0-151">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f2a0-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3f2a0-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f2a0-152">OUTPUTS</span></span>

### <span data-ttu-id="3f2a0-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3f2a0-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3f2a0-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f2a0-154">NOTES</span></span>

## <span data-ttu-id="3f2a0-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f2a0-155">RELATED LINKS</span></span>

[<span data-ttu-id="3f2a0-156">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f2a0-156">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="3f2a0-157">Nowe — AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f2a0-157">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="3f2a0-158">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f2a0-158">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

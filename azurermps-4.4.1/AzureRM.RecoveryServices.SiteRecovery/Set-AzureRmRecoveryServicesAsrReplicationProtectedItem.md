---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 5627b94f87d69fab6b760bf05f1e22566992048b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718123"
---
# <span data-ttu-id="f5f77-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5f77-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="f5f77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5f77-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f77-103">Ustawia właściwości odzyskiwania, takie jak Sieć docelowa i rozmiar maszyny wirtualnej dla określonego elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="f5f77-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5f77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5f77-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5f77-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f77-106">Polecenie cmdlet **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** ustawia właściwości odzyskiwania elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="f5f77-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="f5f77-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5f77-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f77-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5f77-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="f5f77-109">Rozpoczyna operację aktualizowania ustawień elementu ochrony replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="f5f77-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f5f77-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5f77-110">PARAMETERS</span></span>

### <span data-ttu-id="f5f77-111">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5f77-111">-InputObject</span></span>
<span data-ttu-id="f5f77-112">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej replikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f5f77-112">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="f5f77-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f5f77-113">-LicenseType</span></span>
<span data-ttu-id="f5f77-114">Określ typ licencji, który ma być wykorzystywany na potrzeby maszyn wirtualnych systemu Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f5f77-114">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="f5f77-115">Jeśli masz prawo do korzystania z funkcji korzystania z usługi Azure hybrydowego (KONCENTRATORa) do migracji, a chcesz określić, że ustawienie KONCENTRATORa ma być używane podczas nieprzekraczania tego chronionego elementu, ustaw typ licencji na WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="f5f77-115">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="f5f77-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5f77-116">-Name</span></span>
<span data-ttu-id="f5f77-117">Określa nazwę maszyny wirtualnej odzyskiwania, która zostanie utworzona w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="f5f77-117">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="f5f77-118">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="f5f77-118">-NicSelectionType</span></span>
<span data-ttu-id="f5f77-119">Określa właściwości karty interfejsu sieciowego (NIC), które są ustawiane przez użytkownika lub ustawione domyślnie.</span><span class="sxs-lookup"><span data-stu-id="f5f77-119">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="f5f77-120">Możesz określić NotSelected, aby wrócić do wartości domyślnych.</span><span class="sxs-lookup"><span data-stu-id="f5f77-120">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="f5f77-121">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="f5f77-121">-PrimaryNic</span></span>
<span data-ttu-id="f5f77-122">Określa kartę sieciową maszyny wirtualnej, dla której to polecenie cmdlet ustawia właściwość sieć odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f5f77-122">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="f5f77-123">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="f5f77-123">-RecoveryNetworkId</span></span>
<span data-ttu-id="f5f77-124">Określa identyfikator sieci wirtualnej platformy Azure, do której należy przejść w celu przekroczenia ochrony elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="f5f77-124">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="f5f77-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="f5f77-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="f5f77-126">Określa statyczny adres IP, który powinien być przypisany do podstawowej karty sieciowej przy odzyskiwaniu.</span><span class="sxs-lookup"><span data-stu-id="f5f77-126">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="f5f77-127">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="f5f77-127">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="f5f77-128">Określa nazwę podsieci w wirtualnej sieci Azure, do której ma być podłączona ta karta sieciowa chronionego elementu w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="f5f77-128">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="f5f77-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f5f77-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="f5f77-130">Identyfikator grupy zasobów platformy Azure w regionie odzyskiwania, w którym chroniony element zostanie przywrócony po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f5f77-130">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="f5f77-131">-Size</span><span class="sxs-lookup"><span data-stu-id="f5f77-131">-Size</span></span>
<span data-ttu-id="f5f77-132">Określa rozmiar maszyny wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f5f77-132">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="f5f77-133">Wartość powinna pochodzić z zestawu rozmiarów obsługiwanych przez maszyny wirtualne platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f77-133">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="f5f77-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5f77-134">-Confirm</span></span>
<span data-ttu-id="f5f77-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f77-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f77-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f77-136">-WhatIf</span></span>
<span data-ttu-id="f5f77-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f77-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5f77-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5f77-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f77-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f77-139">CommonParameters</span></span>
<span data-ttu-id="f5f77-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f77-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f77-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f77-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f77-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5f77-142">INPUTS</span></span>

### <span data-ttu-id="f5f77-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5f77-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f5f77-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5f77-144">OUTPUTS</span></span>

### <span data-ttu-id="f5f77-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f5f77-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f5f77-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5f77-146">NOTES</span></span>

## <span data-ttu-id="f5f77-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5f77-147">RELATED LINKS</span></span>

[<span data-ttu-id="f5f77-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5f77-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f5f77-149">Nowe — AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5f77-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f5f77-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5f77-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 11598952da67d7f3b3ec94f6c64b71c80bbad12c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708582"
---
# <span data-ttu-id="f5206-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5206-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="f5206-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5206-102">SYNOPSIS</span></span>
<span data-ttu-id="f5206-103">Ustawia właściwości odzyskiwania, takie jak Sieć docelowa i rozmiar maszyny wirtualnej dla określonego elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="f5206-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="f5206-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5206-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryCloudServiceId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-RecoveryAvailabilitySet <String>]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5206-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5206-105">DESCRIPTION</span></span>
<span data-ttu-id="f5206-106">Polecenie cmdlet **Set-AzRecoveryServicesAsrReplicationProtectedItem** ustawia właściwości odzyskiwania elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="f5206-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="f5206-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5206-107">EXAMPLES</span></span>

### <span data-ttu-id="f5206-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5206-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="f5206-109">Rozpoczyna operację aktualizowania ustawień elementu ochrony replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="f5206-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f5206-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5206-110">PARAMETERS</span></span>

### <span data-ttu-id="f5206-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5206-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="f5206-112">{{Fill AzureToAzureUpdateReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="f5206-112">{{Fill AzureToAzureUpdateReplicationConfiguration Description}}</span></span>

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

### <span data-ttu-id="f5206-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5206-113">-DefaultProfile</span></span>
<span data-ttu-id="f5206-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5206-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f5206-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5206-115">-InputObject</span></span>
<span data-ttu-id="f5206-116">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej replikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f5206-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="f5206-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f5206-117">-LicenseType</span></span>
<span data-ttu-id="f5206-118">Określ typ licencji, który ma być wykorzystywany na potrzeby maszyn wirtualnych systemu Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f5206-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="f5206-119">Jeśli masz prawo do korzystania z funkcji korzystania z usługi Azure hybrydowego (KONCENTRATORa) do migracji, a chcesz określić, że ustawienie KONCENTRATORa ma być używane podczas nieprzekraczania tego chronionego elementu, ustaw typ licencji na WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="f5206-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="f5206-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5206-120">-Name</span></span>
<span data-ttu-id="f5206-121">Określa nazwę maszyny wirtualnej odzyskiwania, która zostanie utworzona w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="f5206-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="f5206-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="f5206-122">-NicSelectionType</span></span>
<span data-ttu-id="f5206-123">Określa właściwości karty interfejsu sieciowego (NIC), które są ustawiane przez użytkownika lub ustawione domyślnie.</span><span class="sxs-lookup"><span data-stu-id="f5206-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="f5206-124">Możesz określić NotSelected, aby wrócić do wartości domyślnych.</span><span class="sxs-lookup"><span data-stu-id="f5206-124">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="f5206-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="f5206-125">-PrimaryNic</span></span>
<span data-ttu-id="f5206-126">Określa kartę sieciową maszyny wirtualnej, dla której to polecenie cmdlet ustawia właściwość sieć odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f5206-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="f5206-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f5206-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="f5206-128">Zestaw dostępności dla elementu chronionego replikacji po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f5206-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="f5206-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f5206-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="f5206-130">Określa konto magazynu do diagnostyki rozruchu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f5206-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="f5206-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="f5206-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="f5206-132">Identyfikator zasobu usługi w chmurze odzyskiwania, do której ma zostać przejdzie przejście do tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5206-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="f5206-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="f5206-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="f5206-134">Określa identyfikator sieci wirtualnej platformy Azure, do której należy przejść w celu przekroczenia ochrony elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="f5206-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="f5206-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="f5206-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="f5206-136">Określa statyczny adres IP, który powinien być przypisany do podstawowej karty sieciowej przy odzyskiwaniu.</span><span class="sxs-lookup"><span data-stu-id="f5206-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="f5206-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="f5206-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="f5206-138">Określa nazwę podsieci w wirtualnej sieci Azure, do której ma być podłączona ta karta sieciowa chronionego elementu w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="f5206-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="f5206-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f5206-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="f5206-140">Identyfikator grupy zasobów platformy Azure w regionie odzyskiwania, w którym chroniony element zostanie przywrócony po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f5206-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="f5206-141">-Size</span><span class="sxs-lookup"><span data-stu-id="f5206-141">-Size</span></span>
<span data-ttu-id="f5206-142">Określa rozmiar maszyny wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f5206-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="f5206-143">Wartość powinna pochodzić z zestawu rozmiarów obsługiwanych przez maszyny wirtualne platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f5206-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="f5206-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f5206-144">-UseManagedDisk</span></span>
<span data-ttu-id="f5206-145">Określa, czy maszyna wirtualna Azure utworzona w trybie failover powinna korzystać z dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="f5206-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="f5206-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5206-146">-Confirm</span></span>
<span data-ttu-id="f5206-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5206-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5206-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5206-148">-WhatIf</span></span>
<span data-ttu-id="f5206-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5206-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5206-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5206-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5206-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5206-151">CommonParameters</span></span>
<span data-ttu-id="f5206-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5206-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5206-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5206-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5206-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5206-154">INPUTS</span></span>

### <span data-ttu-id="f5206-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5206-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f5206-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5206-156">OUTPUTS</span></span>

### <span data-ttu-id="f5206-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f5206-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f5206-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5206-158">NOTES</span></span>

## <span data-ttu-id="f5206-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5206-159">RELATED LINKS</span></span>

[<span data-ttu-id="f5206-160">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5206-160">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f5206-161">Nowe — AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5206-161">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f5206-162">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5206-162">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

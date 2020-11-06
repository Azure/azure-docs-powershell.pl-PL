---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: bab9cb87f347b198b430c1dadc65a002dfa94141
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525002"
---
# <span data-ttu-id="e9a76-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e9a76-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="e9a76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9a76-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a76-103">Rozpoczyna operację testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="e9a76-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9a76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9a76-104">SYNTAX</span></span>

### <span data-ttu-id="e9a76-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e9a76-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a76-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e9a76-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a76-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e9a76-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a76-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e9a76-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a76-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e9a76-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a76-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e9a76-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9a76-111">Opis</span><span class="sxs-lookup"><span data-stu-id="e9a76-111">DESCRIPTION</span></span>
<span data-ttu-id="e9a76-112">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** rozpoczyna test pracy awaryjnej w trybie failover witryny usługi Azure chronionej przed replikacją lub planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e9a76-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="e9a76-113">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9a76-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="e9a76-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9a76-114">EXAMPLES</span></span>

### <span data-ttu-id="e9a76-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e9a76-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="e9a76-116">Rozpoczyna operację testowej pracy w trybie failover dla planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="e9a76-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e9a76-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9a76-117">PARAMETERS</span></span>

### <span data-ttu-id="e9a76-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e9a76-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="e9a76-119">Określa identyfikator sieci wirtualnej platformy Azure, w którym można połączyć test zakończony niepowodzeniem na maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="e9a76-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a76-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="e9a76-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="e9a76-121">Określa, czy należy utworzyć nową usługę w chmurze, czy należy użyć usługi chmury odzyskiwania skonfigurowanej dla maszyny wirtualnej na potrzeby testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="e9a76-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a76-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9a76-122">-Confirm</span></span>
<span data-ttu-id="e9a76-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9a76-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a76-124">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e9a76-124">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="e9a76-125">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e9a76-125">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="e9a76-126">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e9a76-126">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="e9a76-127">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e9a76-127">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="e9a76-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a76-128">-DefaultProfile</span></span>
<span data-ttu-id="e9a76-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a76-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="e9a76-130">-Direction</span><span class="sxs-lookup"><span data-stu-id="e9a76-130">-Direction</span></span>
<span data-ttu-id="e9a76-131">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="e9a76-131">Specifies the failover direction.</span></span>
<span data-ttu-id="e9a76-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e9a76-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9a76-133">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e9a76-133">PrimaryToRecovery</span></span>
- <span data-ttu-id="e9a76-134">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e9a76-134">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a76-135">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e9a76-135">-RecoveryPlan</span></span>
<span data-ttu-id="e9a76-136">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="e9a76-136">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a76-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e9a76-137">-RecoveryPoint</span></span>
<span data-ttu-id="e9a76-138">Umożliwia określenie niestandardowego punktu odzyskiwania w celu przetestowania trybu failover chronionego komputera.</span><span class="sxs-lookup"><span data-stu-id="e9a76-138">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a76-139">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="e9a76-139">-RecoveryTag</span></span>
<span data-ttu-id="e9a76-140">Określa znacznik odzyskiwania w celu przetestowania trybu failover na</span><span class="sxs-lookup"><span data-stu-id="e9a76-140">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a76-141">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e9a76-141">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e9a76-142">Określa element chroniony replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="e9a76-142">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a76-143">-Sieć VMNetwork</span><span class="sxs-lookup"><span data-stu-id="e9a76-143">-VMNetwork</span></span>
<span data-ttu-id="e9a76-144">Określa sieć maszyny wirtualnej odzyskiwania witryny, do której mają być połączone maszyny wirtualne testowe w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="e9a76-144">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a76-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a76-145">-WhatIf</span></span>
<span data-ttu-id="e9a76-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9a76-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9a76-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9a76-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a76-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a76-148">CommonParameters</span></span>
<span data-ttu-id="e9a76-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a76-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a76-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9a76-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a76-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9a76-151">INPUTS</span></span>

### <span data-ttu-id="e9a76-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e9a76-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="e9a76-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e9a76-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e9a76-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9a76-154">OUTPUTS</span></span>

### <span data-ttu-id="e9a76-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e9a76-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e9a76-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9a76-156">NOTES</span></span>

## <span data-ttu-id="e9a76-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9a76-157">RELATED LINKS</span></span>

[<span data-ttu-id="e9a76-158">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e9a76-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

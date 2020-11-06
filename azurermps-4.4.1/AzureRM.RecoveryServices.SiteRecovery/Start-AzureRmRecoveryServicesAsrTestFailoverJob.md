---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550827"
---
# <span data-ttu-id="8da87-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8da87-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="8da87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8da87-102">SYNOPSIS</span></span>
<span data-ttu-id="8da87-103">Rozpoczyna operację testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="8da87-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8da87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8da87-104">SYNTAX</span></span>

### <span data-ttu-id="8da87-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8da87-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da87-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8da87-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8da87-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8da87-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da87-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8da87-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da87-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8da87-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da87-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8da87-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da87-111">Opis</span><span class="sxs-lookup"><span data-stu-id="8da87-111">DESCRIPTION</span></span>
<span data-ttu-id="8da87-112">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** rozpoczyna test pracy awaryjnej w trybie failover witryny usługi Azure chronionej przed replikacją lub planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8da87-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="8da87-113">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da87-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="8da87-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8da87-114">EXAMPLES</span></span>

### <span data-ttu-id="8da87-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8da87-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="8da87-116">Rozpoczyna operację testowej pracy w trybie failover dla planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="8da87-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8da87-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8da87-117">PARAMETERS</span></span>

### <span data-ttu-id="8da87-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8da87-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="8da87-119">Określa identyfikator sieci wirtualnej platformy Azure, w którym można połączyć test zakończony niepowodzeniem na maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="8da87-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

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

### <span data-ttu-id="8da87-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8da87-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8da87-121">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8da87-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="8da87-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8da87-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8da87-123">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8da87-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="8da87-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="8da87-124">-Direction</span></span>
<span data-ttu-id="8da87-125">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="8da87-125">Specifies the failover direction.</span></span>
<span data-ttu-id="8da87-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8da87-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8da87-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="8da87-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="8da87-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="8da87-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="8da87-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8da87-129">-RecoveryPlan</span></span>
<span data-ttu-id="8da87-130">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="8da87-130">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="8da87-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8da87-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8da87-132">Określa element chroniony replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="8da87-132">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="8da87-133">-Sieć VMNetwork</span><span class="sxs-lookup"><span data-stu-id="8da87-133">-VMNetwork</span></span>
<span data-ttu-id="8da87-134">Określa sieć maszyny wirtualnej odzyskiwania witryny, do której mają być połączone maszyny wirtualne testowe w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="8da87-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="8da87-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8da87-135">-Confirm</span></span>
<span data-ttu-id="8da87-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da87-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da87-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da87-137">-WhatIf</span></span>
<span data-ttu-id="8da87-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da87-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8da87-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8da87-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da87-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da87-140">CommonParameters</span></span>
<span data-ttu-id="8da87-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da87-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da87-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da87-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da87-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8da87-143">INPUTS</span></span>

### <span data-ttu-id="8da87-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8da87-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="8da87-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8da87-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8da87-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8da87-146">OUTPUTS</span></span>

### <span data-ttu-id="8da87-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8da87-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8da87-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8da87-148">NOTES</span></span>

## <span data-ttu-id="8da87-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8da87-149">RELATED LINKS</span></span>

[<span data-ttu-id="8da87-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8da87-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

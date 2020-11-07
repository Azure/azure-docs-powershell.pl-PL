---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718122"
---
# <span data-ttu-id="68c31-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="68c31-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="68c31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68c31-102">SYNOPSIS</span></span>
<span data-ttu-id="68c31-103">Rozpoczyna nieplanowaną operację pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="68c31-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68c31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68c31-104">SYNTAX</span></span>

### <span data-ttu-id="68c31-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="68c31-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68c31-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="68c31-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68c31-107">Opis</span><span class="sxs-lookup"><span data-stu-id="68c31-107">DESCRIPTION</span></span>
<span data-ttu-id="68c31-108">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** uruchamia nieplanowaną pracę awaryjną w trybie failover witryny usługi Azure chronionej przed replikacją lub planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="68c31-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="68c31-109">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68c31-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="68c31-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68c31-110">EXAMPLES</span></span>

### <span data-ttu-id="68c31-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="68c31-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="68c31-112">Rozpoczyna nieplanowaną operację pracy awaryjnej dla określonego planu odzyskiwania przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="68c31-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="68c31-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68c31-113">PARAMETERS</span></span>

### <span data-ttu-id="68c31-114">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="68c31-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="68c31-115">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="68c31-115">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="68c31-116">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="68c31-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="68c31-117">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="68c31-117">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="68c31-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="68c31-118">-Direction</span></span>
<span data-ttu-id="68c31-119">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="68c31-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="68c31-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="68c31-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68c31-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="68c31-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="68c31-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="68c31-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="68c31-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="68c31-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="68c31-124">Wskazuje, że należy podjąć próbę wykonania dowolnej operacji witryny źródłowej określonej w planie odzyskiwania w ramach funkcji pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="68c31-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c31-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="68c31-125">-RecoveryPlan</span></span>
<span data-ttu-id="68c31-126">Określa obiekt planu odzyskiwania ASR odpowiadający planowi odzyskiwania, na którym ma być przeprowadzana operacja przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="68c31-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="68c31-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="68c31-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="68c31-128">Określa obiekt elementu chronionego replikacji ASR, który odpowiada elementowi chronionej replikacji, dla którego ma zostać wykonana operacja przejęcia awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="68c31-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68c31-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68c31-129">-Confirm</span></span>
<span data-ttu-id="68c31-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68c31-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68c31-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68c31-131">-WhatIf</span></span>
<span data-ttu-id="68c31-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68c31-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68c31-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68c31-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68c31-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c31-134">CommonParameters</span></span>
<span data-ttu-id="68c31-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68c31-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c31-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68c31-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c31-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68c31-137">INPUTS</span></span>

### <span data-ttu-id="68c31-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="68c31-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="68c31-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="68c31-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="68c31-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68c31-140">OUTPUTS</span></span>

### <span data-ttu-id="68c31-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="68c31-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68c31-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68c31-142">NOTES</span></span>

## <span data-ttu-id="68c31-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68c31-143">RELATED LINKS</span></span>

[<span data-ttu-id="68c31-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="68c31-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)



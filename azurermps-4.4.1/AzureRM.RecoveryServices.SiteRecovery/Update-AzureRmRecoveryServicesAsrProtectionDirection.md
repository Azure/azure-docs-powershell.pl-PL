---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718116"
---
# <span data-ttu-id="0f607-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="0f607-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="0f607-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f607-102">SYNOPSIS</span></span>
<span data-ttu-id="0f607-103">Aktualizuje kierunek replikacji określonego elementu chronionego replikacji lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0f607-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="0f607-104">Służy do ponownego zabezpieczania/odtwarzania kopii zapasowej w replikowanym elemencie lub planie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0f607-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f607-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f607-105">SYNTAX</span></span>

### <span data-ttu-id="0f607-106">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f607-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f607-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0f607-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f607-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="0f607-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f607-109">Opis</span><span class="sxs-lookup"><span data-stu-id="0f607-109">DESCRIPTION</span></span>
<span data-ttu-id="0f607-110">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrProtectionDirection** aktualizuje kierunek replikacji określonego obiektu odzyskiwania witryny platformy Azure po zakończeniu operacji zatwierdzania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="0f607-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="0f607-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f607-111">EXAMPLES</span></span>

### <span data-ttu-id="0f607-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f607-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="0f607-113">Rozpocznij operację zmiany kierunku aktualizacji dla określonego planu Recoveyr i zwraca obiekt zadania ASR, którego użyto do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="0f607-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="0f607-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f607-114">PARAMETERS</span></span>

### <span data-ttu-id="0f607-115">-Direction</span><span class="sxs-lookup"><span data-stu-id="0f607-115">-Direction</span></span>
<span data-ttu-id="0f607-116">Określa kierunek, w jakim operacja aktualizacji służy do zaksięgowania pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="0f607-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="0f607-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0f607-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f607-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0f607-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="0f607-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0f607-119">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="0f607-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0f607-120">-RecoveryPlan</span></span>
<span data-ttu-id="0f607-121">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="0f607-121">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="0f607-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0f607-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0f607-123">Określa element chroniony replikacji ASR</span><span class="sxs-lookup"><span data-stu-id="0f607-123">Specifies an ASR replication protected item</span></span>

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

### <span data-ttu-id="0f607-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f607-124">-Confirm</span></span>
<span data-ttu-id="0f607-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f607-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f607-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f607-126">-WhatIf</span></span>
<span data-ttu-id="0f607-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f607-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f607-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f607-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f607-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f607-129">CommonParameters</span></span>
<span data-ttu-id="0f607-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f607-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f607-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f607-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f607-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f607-132">INPUTS</span></span>

### <span data-ttu-id="0f607-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0f607-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="0f607-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0f607-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0f607-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f607-135">OUTPUTS</span></span>

### <span data-ttu-id="0f607-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0f607-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0f607-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f607-137">NOTES</span></span>

## <span data-ttu-id="0f607-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f607-138">RELATED LINKS</span></span>


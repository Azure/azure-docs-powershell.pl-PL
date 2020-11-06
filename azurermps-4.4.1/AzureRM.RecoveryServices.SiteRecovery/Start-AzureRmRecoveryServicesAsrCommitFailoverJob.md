---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549932"
---
# <span data-ttu-id="4cbbb-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="4cbbb-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="4cbbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbbb-103">Rozpoczyna akcję zatwierdzania trybu failover dla obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cbbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cbbb-104">SYNTAX</span></span>

### <span data-ttu-id="4cbbb-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4cbbb-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cbbb-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4cbbb-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cbbb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4cbbb-107">DESCRIPTION</span></span>
<span data-ttu-id="4cbbb-108">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** uruchamia proces zatwierdzania trybu failover dla obiektu odzyskiwania witryny Azure po wykonaniu operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="4cbbb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cbbb-109">EXAMPLES</span></span>

### <span data-ttu-id="4cbbb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4cbbb-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="4cbbb-111">Rozpoczyna przechodzenie do trybu failover dla określonego planu odzyskiwania i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4cbbb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cbbb-112">PARAMETERS</span></span>

### <span data-ttu-id="4cbbb-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4cbbb-113">-RecoveryPlan</span></span>
<span data-ttu-id="4cbbb-114">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-114">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="4cbbb-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4cbbb-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4cbbb-116">Określa obiekt elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-116">Specifies an ASR replication protected item object.</span></span>

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

### <span data-ttu-id="4cbbb-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cbbb-117">-Confirm</span></span>
<span data-ttu-id="4cbbb-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cbbb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cbbb-119">-WhatIf</span></span>
<span data-ttu-id="4cbbb-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cbbb-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cbbb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbbb-122">CommonParameters</span></span>
<span data-ttu-id="4cbbb-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbbb-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbbb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbbb-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cbbb-125">INPUTS</span></span>

### <span data-ttu-id="4cbbb-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4cbbb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="4cbbb-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4cbbb-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4cbbb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cbbb-128">OUTPUTS</span></span>

### <span data-ttu-id="4cbbb-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4cbbb-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4cbbb-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cbbb-130">NOTES</span></span>

## <span data-ttu-id="4cbbb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cbbb-131">RELATED LINKS</span></span>


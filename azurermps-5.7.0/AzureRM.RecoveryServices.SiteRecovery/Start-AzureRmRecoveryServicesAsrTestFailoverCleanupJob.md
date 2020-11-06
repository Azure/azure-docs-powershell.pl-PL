---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 423ec89745b21176c714c1c2e956d4320c28b034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525005"
---
# <span data-ttu-id="7430f-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="7430f-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="7430f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7430f-102">SYNOPSIS</span></span>
<span data-ttu-id="7430f-103">Rozpoczyna operację sprawdzania oczyszczania w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="7430f-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7430f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7430f-104">SYNTAX</span></span>

### <span data-ttu-id="7430f-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7430f-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7430f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7430f-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7430f-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7430f-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7430f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7430f-108">DESCRIPTION</span></span>
<span data-ttu-id="7430f-109">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** rozpoczyna operację sprawdzania oczyszczania pracy awaryjnej w elemencie chronionym replikacji lub w planie odzyskiwania, na którym przeprowadzono test pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="7430f-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="7430f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7430f-110">EXAMPLES</span></span>

### <span data-ttu-id="7430f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7430f-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="7430f-112">Zadanie śledzenia oczyszczania testowej pracy awaryjnej elementu chronionej replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7430f-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="7430f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7430f-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $recoveryPlan -Comments "testing done"
```

<span data-ttu-id="7430f-114">Zadanie śledzenia oczyszczania testowej pracy awaryjnej usługi Azure Site Recovery recoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="7430f-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="7430f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7430f-115">PARAMETERS</span></span>

### <span data-ttu-id="7430f-116">-Komentarz</span><span class="sxs-lookup"><span data-stu-id="7430f-116">-Comment</span></span>
<span data-ttu-id="7430f-117">Komentarz użytkownika dotyczący testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="7430f-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="7430f-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7430f-118">-Confirm</span></span>
<span data-ttu-id="7430f-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7430f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7430f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7430f-120">-DefaultProfile</span></span>
<span data-ttu-id="7430f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7430f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7430f-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7430f-122">-RecoveryPlan</span></span>
<span data-ttu-id="7430f-123">Plan odzyskiwania umożliwiający przeprowadzenie testowego oczyszczania pracy awaryjnej w dniu.</span><span class="sxs-lookup"><span data-stu-id="7430f-123">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="7430f-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7430f-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7430f-125">Chroniony element replikacji, aby wykonać testową operację oczyszczania w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="7430f-125">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="7430f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7430f-126">-ResourceId</span></span>
<span data-ttu-id="7430f-127">Identyfikator zasobu chronionego planu elementów/odzyskiwania usługi replikacji cleaningup testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="7430f-127">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7430f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7430f-128">-WhatIf</span></span>
<span data-ttu-id="7430f-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7430f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7430f-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7430f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7430f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7430f-131">CommonParameters</span></span>
<span data-ttu-id="7430f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7430f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7430f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7430f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7430f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7430f-134">INPUTS</span></span>

### <span data-ttu-id="7430f-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7430f-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="7430f-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7430f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7430f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7430f-137">OUTPUTS</span></span>

### <span data-ttu-id="7430f-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7430f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7430f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7430f-139">NOTES</span></span>

## <span data-ttu-id="7430f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7430f-140">RELATED LINKS</span></span>

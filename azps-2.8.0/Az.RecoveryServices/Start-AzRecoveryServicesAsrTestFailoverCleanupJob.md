---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 4143bc481091889b293d206192e0c5eba386d68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886586"
---
# <span data-ttu-id="59de0-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="59de0-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="59de0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59de0-102">SYNOPSIS</span></span>
<span data-ttu-id="59de0-103">Rozpoczyna operację sprawdzania oczyszczania w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="59de0-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="59de0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59de0-104">SYNTAX</span></span>

### <span data-ttu-id="59de0-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="59de0-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59de0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59de0-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59de0-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="59de0-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59de0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="59de0-108">DESCRIPTION</span></span>
<span data-ttu-id="59de0-109">Polecenie cmdlet **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** rozpoczyna operację sprawdzania oczyszczania pracy awaryjnej w elemencie chronionym replikacji lub w planie odzyskiwania, na którym przeprowadzono test pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="59de0-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="59de0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59de0-110">EXAMPLES</span></span>

### <span data-ttu-id="59de0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59de0-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="59de0-112">Zadanie śledzenia oczyszczania testowej pracy awaryjnej elementu chronionej replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="59de0-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="59de0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="59de0-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="59de0-114">Zadanie śledzenia oczyszczania testowej pracy awaryjnej usługi Azure Site Recovery recoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="59de0-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="59de0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59de0-115">PARAMETERS</span></span>

### <span data-ttu-id="59de0-116">-Komentarz</span><span class="sxs-lookup"><span data-stu-id="59de0-116">-Comment</span></span>
<span data-ttu-id="59de0-117">Komentarz użytkownika dotyczący testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="59de0-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="59de0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59de0-118">-DefaultProfile</span></span>
<span data-ttu-id="59de0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59de0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59de0-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="59de0-120">-RecoveryPlan</span></span>
<span data-ttu-id="59de0-121">Plan odzyskiwania umożliwiający przeprowadzenie testowego oczyszczania pracy awaryjnej w dniu.</span><span class="sxs-lookup"><span data-stu-id="59de0-121">Recovery Plan to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59de0-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="59de0-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="59de0-123">Chroniony element replikacji, aby wykonać testową operację oczyszczania w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="59de0-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59de0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59de0-124">-ResourceId</span></span>
<span data-ttu-id="59de0-125">Identyfikator zasobu chronionego planu elementów/odzyskiwania usługi replikacji cleaningup testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="59de0-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59de0-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59de0-126">-Confirm</span></span>
<span data-ttu-id="59de0-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59de0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59de0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59de0-128">-WhatIf</span></span>
<span data-ttu-id="59de0-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59de0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59de0-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59de0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59de0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59de0-131">CommonParameters</span></span>
<span data-ttu-id="59de0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59de0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59de0-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59de0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59de0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59de0-134">INPUTS</span></span>

### <span data-ttu-id="59de0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="59de0-135">System.String</span></span>

### <span data-ttu-id="59de0-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="59de0-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="59de0-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="59de0-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="59de0-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59de0-138">OUTPUTS</span></span>

### <span data-ttu-id="59de0-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="59de0-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="59de0-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59de0-140">NOTES</span></span>

## <span data-ttu-id="59de0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59de0-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 68e06f8a4d9c88b57fa88ee8044ca2e5d04d9ce9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552375"
---
# <span data-ttu-id="119d2-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="119d2-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="119d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="119d2-102">SYNOPSIS</span></span>
<span data-ttu-id="119d2-103">Umożliwia edytowanie planu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="119d2-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="119d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="119d2-104">SYNTAX</span></span>

### <span data-ttu-id="119d2-105">Append (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="119d2-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="119d2-106">Usuń</span><span class="sxs-lookup"><span data-stu-id="119d2-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="119d2-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="119d2-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="119d2-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="119d2-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="119d2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="119d2-109">DESCRIPTION</span></span>
<span data-ttu-id="119d2-110">Polecenie cmdlet **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** edytuje plan odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="119d2-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="119d2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="119d2-111">EXAMPLES</span></span>

### <span data-ttu-id="119d2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="119d2-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="119d2-113">Dołącza grupę do istniejącego planu odzyskiwania usługi Azure Site Recovery i zwraca zaktualizowany plan odzyskiwania w pamięci.</span><span class="sxs-lookup"><span data-stu-id="119d2-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="119d2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="119d2-114">PARAMETERS</span></span>

### <span data-ttu-id="119d2-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="119d2-115">-AddProtectedItem</span></span>
<span data-ttu-id="119d2-116">Lista elementów chronionych replikacji ASR, które mają zostać dodane do grupy plan odzyskiwania w obiekcie plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="119d2-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="119d2-117">-Append</span><span class="sxs-lookup"><span data-stu-id="119d2-117">-AppendGroup</span></span>
<span data-ttu-id="119d2-118">Parametr Przełącz umożliwiający dołączenie grupy planu odzyskiwania do obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="119d2-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="119d2-119">-Group</span><span class="sxs-lookup"><span data-stu-id="119d2-119">-Group</span></span>
<span data-ttu-id="119d2-120">Określa grupę planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="119d2-120">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="119d2-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="119d2-121">-InputObject</span></span>
<span data-ttu-id="119d2-122">Obiekt planu odzyskiwania ASR, który ma być edytowany (w ramach operacji pamięci.</span><span class="sxs-lookup"><span data-stu-id="119d2-122">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="119d2-123">Aby zaktualizować plan odzyskiwania Update-AzureRmASRRecoveryPlan Uruchom obiekt z edytowanym planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="119d2-123">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="119d2-124">-Remove</span><span class="sxs-lookup"><span data-stu-id="119d2-124">-RemoveGroup</span></span>
<span data-ttu-id="119d2-125">Usuwa określoną grupę z obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="119d2-125">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="119d2-126">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="119d2-126">-RemoveProtectedItem</span></span>
<span data-ttu-id="119d2-127">Lista elementów chronionych replikacji ASR do usunięcia z grupy plan odzyskiwania w obiekcie plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="119d2-127">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="119d2-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="119d2-128">-Confirm</span></span>
<span data-ttu-id="119d2-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="119d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="119d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="119d2-130">-WhatIf</span></span>
<span data-ttu-id="119d2-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="119d2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="119d2-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="119d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="119d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="119d2-133">CommonParameters</span></span>
<span data-ttu-id="119d2-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="119d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="119d2-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="119d2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="119d2-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="119d2-136">INPUTS</span></span>

### <span data-ttu-id="119d2-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="119d2-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="119d2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="119d2-138">OUTPUTS</span></span>

### <span data-ttu-id="119d2-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="119d2-139">System.Object</span></span>

## <span data-ttu-id="119d2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="119d2-140">NOTES</span></span>

## <span data-ttu-id="119d2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="119d2-141">RELATED LINKS</span></span>

[<span data-ttu-id="119d2-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="119d2-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="119d2-143">Nowe — AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="119d2-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: be66887225ee78b31497bbd8918faae9535731de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896146"
---
# <span data-ttu-id="c7c1f-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c7c1f-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="c7c1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c1f-103">Umożliwia edytowanie planu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="c7c1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7c1f-104">SYNTAX</span></span>

### <span data-ttu-id="c7c1f-105">Append (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c7c1f-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c1f-106">Usuń</span><span class="sxs-lookup"><span data-stu-id="c7c1f-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c1f-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="c7c1f-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c1f-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="c7c1f-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7c1f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c7c1f-109">DESCRIPTION</span></span>
<span data-ttu-id="c7c1f-110">Polecenie cmdlet **Edit-AzRecoveryServicesAsrRecoveryPlan** edytuje plan odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="c7c1f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7c1f-111">EXAMPLES</span></span>

### <span data-ttu-id="c7c1f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7c1f-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="c7c1f-113">Dołącza grupę do istniejącego planu odzyskiwania witryny platformy Azure i zwraca zaktualizowany plan odzyskiwania w pamięci.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-113">Appends a group to existing Azure Site Recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="c7c1f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7c1f-114">PARAMETERS</span></span>

### <span data-ttu-id="c7c1f-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c7c1f-115">-AddProtectedItem</span></span>
<span data-ttu-id="c7c1f-116">Lista elementów chronionych replikacji ASR, które mają zostać dodane do grupy plan odzyskiwania w obiekcie plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c1f-117">-Append</span><span class="sxs-lookup"><span data-stu-id="c7c1f-117">-AppendGroup</span></span>
<span data-ttu-id="c7c1f-118">Parametr Przełącz umożliwiający dołączenie grupy planu odzyskiwania do obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c1f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c1f-119">-DefaultProfile</span></span>
<span data-ttu-id="c7c1f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c7c1f-121">-Group</span><span class="sxs-lookup"><span data-stu-id="c7c1f-121">-Group</span></span>
<span data-ttu-id="c7c1f-122">Określa grupę planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c1f-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7c1f-123">-InputObject</span></span>
<span data-ttu-id="c7c1f-124">Obiekt planu odzyskiwania ASR, który ma być edytowany (w ramach operacji pamięci.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="c7c1f-125">Aby zaktualizować plan odzyskiwania Update-AzASRRecoveryPlan Uruchom obiekt z edytowanym planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c1f-126">-Remove</span><span class="sxs-lookup"><span data-stu-id="c7c1f-126">-RemoveGroup</span></span>
<span data-ttu-id="c7c1f-127">Usuwa określoną grupę z obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c1f-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c7c1f-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="c7c1f-129">Lista elementów chronionych replikacji ASR do usunięcia z grupy plan odzyskiwania w obiekcie plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c1f-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7c1f-130">-Confirm</span></span>
<span data-ttu-id="c7c1f-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7c1f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c1f-132">-WhatIf</span></span>
<span data-ttu-id="c7c1f-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7c1f-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7c1f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c1f-135">CommonParameters</span></span>
<span data-ttu-id="c7c1f-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c1f-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7c1f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c1f-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7c1f-138">INPUTS</span></span>

### <span data-ttu-id="c7c1f-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c7c1f-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="c7c1f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7c1f-140">OUTPUTS</span></span>

### <span data-ttu-id="c7c1f-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c7c1f-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="c7c1f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7c1f-142">NOTES</span></span>

## <span data-ttu-id="c7c1f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7c1f-143">RELATED LINKS</span></span>

[<span data-ttu-id="c7c1f-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c7c1f-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c7c1f-145">Nowe — AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c7c1f-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

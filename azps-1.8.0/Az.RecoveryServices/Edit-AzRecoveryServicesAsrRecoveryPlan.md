---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: cac83004dc56b8d32acacced0339068a1fd932f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708718"
---
# <span data-ttu-id="da740-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da740-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="da740-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da740-102">SYNOPSIS</span></span>
<span data-ttu-id="da740-103">Umożliwia edytowanie planu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="da740-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="da740-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da740-104">SYNTAX</span></span>

### <span data-ttu-id="da740-105">Append (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="da740-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da740-106">Usuń</span><span class="sxs-lookup"><span data-stu-id="da740-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da740-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="da740-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da740-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="da740-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da740-109">Opis</span><span class="sxs-lookup"><span data-stu-id="da740-109">DESCRIPTION</span></span>
<span data-ttu-id="da740-110">Polecenie cmdlet **Edit-AzRecoveryServicesAsrRecoveryPlan** edytuje plan odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da740-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="da740-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da740-111">EXAMPLES</span></span>

### <span data-ttu-id="da740-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da740-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="da740-113">Dołącza grupę do istniejącego planu odzyskiwania usługi Azure Site Recovery i zwraca zaktualizowany plan odzyskiwania w pamięci.</span><span class="sxs-lookup"><span data-stu-id="da740-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="da740-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da740-114">PARAMETERS</span></span>

### <span data-ttu-id="da740-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="da740-115">-AddProtectedItem</span></span>
<span data-ttu-id="da740-116">Lista elementów chronionych replikacji ASR, które mają zostać dodane do grupy plan odzyskiwania w obiekcie plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="da740-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="da740-117">-Append</span><span class="sxs-lookup"><span data-stu-id="da740-117">-AppendGroup</span></span>
<span data-ttu-id="da740-118">Parametr Przełącz umożliwiający dołączenie grupy planu odzyskiwania do obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="da740-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="da740-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da740-119">-DefaultProfile</span></span>
<span data-ttu-id="da740-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da740-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="da740-121">-Group</span><span class="sxs-lookup"><span data-stu-id="da740-121">-Group</span></span>
<span data-ttu-id="da740-122">Określa grupę planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="da740-122">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="da740-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da740-123">-InputObject</span></span>
<span data-ttu-id="da740-124">Obiekt planu odzyskiwania ASR, który ma być edytowany (w ramach operacji pamięci.</span><span class="sxs-lookup"><span data-stu-id="da740-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="da740-125">Aby zaktualizować plan odzyskiwania Update-AzASRRecoveryPlan Uruchom obiekt z edytowanym planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="da740-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="da740-126">-Remove</span><span class="sxs-lookup"><span data-stu-id="da740-126">-RemoveGroup</span></span>
<span data-ttu-id="da740-127">Usuwa określoną grupę z obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="da740-127">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="da740-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="da740-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="da740-129">Lista elementów chronionych replikacji ASR do usunięcia z grupy plan odzyskiwania w obiekcie plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="da740-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="da740-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da740-130">-Confirm</span></span>
<span data-ttu-id="da740-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da740-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da740-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da740-132">-WhatIf</span></span>
<span data-ttu-id="da740-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da740-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da740-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da740-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da740-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da740-135">CommonParameters</span></span>
<span data-ttu-id="da740-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da740-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da740-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da740-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da740-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da740-138">INPUTS</span></span>

### <span data-ttu-id="da740-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da740-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="da740-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da740-140">OUTPUTS</span></span>

### <span data-ttu-id="da740-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da740-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="da740-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da740-142">NOTES</span></span>

## <span data-ttu-id="da740-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da740-143">RELATED LINKS</span></span>

[<span data-ttu-id="da740-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da740-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="da740-145">Nowe — AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da740-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

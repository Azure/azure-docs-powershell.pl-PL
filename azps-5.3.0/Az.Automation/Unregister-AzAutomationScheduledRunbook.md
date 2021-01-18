---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502245"
---
# <span data-ttu-id="081d0-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="081d0-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="081d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="081d0-102">SYNOPSIS</span></span>
<span data-ttu-id="081d0-103">Usuwa skojarzenie między elementem Runbook a harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="081d0-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="081d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="081d0-104">SYNTAX</span></span>

### <span data-ttu-id="081d0-105">ByJobScheduleId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="081d0-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="081d0-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="081d0-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="081d0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="081d0-107">DESCRIPTION</span></span>
<span data-ttu-id="081d0-108">Polecenie cmdlet **Unregister-AzAutomationScheduledRunbook** powoduje usunięcie skojarzenia elementu Runbook usługi Azure Automation i harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="081d0-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="081d0-109">Harmonogram nie będzie już uruchamiał elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="081d0-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="081d0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="081d0-110">EXAMPLES</span></span>

### <span data-ttu-id="081d0-111">Przykład 1: Usuwanie skojarzenia między elementem Runbook a harmonogramem</span><span class="sxs-lookup"><span data-stu-id="081d0-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="081d0-112">To polecenie powoduje usunięcie skojarzenia między elementem Runbook o nazwie Runbk01 a harmonogramem o nazwie Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="081d0-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="081d0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="081d0-113">PARAMETERS</span></span>

### <span data-ttu-id="081d0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="081d0-114">-AutomationAccountName</span></span>
<span data-ttu-id="081d0-115">Określa konto usługi Automation dla elementu Runbook, dla którego działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="081d0-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081d0-116">-DefaultProfile</span></span>
<span data-ttu-id="081d0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="081d0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="081d0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="081d0-118">-Force</span></span>
<span data-ttu-id="081d0-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="081d0-119">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081d0-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="081d0-120">-JobScheduleId</span></span>
<span data-ttu-id="081d0-121">Określa identyfikator zaplanowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="081d0-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="081d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="081d0-123">Określa nazwę grupy zasobów dla zaplanowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="081d0-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081d0-124">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="081d0-124">-RunbookName</span></span>
<span data-ttu-id="081d0-125">Określa nazwę elementu Runbook, który jest niezgodny z harmonogramem tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="081d0-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081d0-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="081d0-126">-ScheduleName</span></span>
<span data-ttu-id="081d0-127">Określa nazwę harmonogramu, z którego to polecenie cmdlet powoduje skojarzenie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="081d0-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081d0-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="081d0-128">-Confirm</span></span>
<span data-ttu-id="081d0-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="081d0-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081d0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="081d0-130">-WhatIf</span></span>
<span data-ttu-id="081d0-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="081d0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="081d0-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="081d0-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081d0-133">CommonParameters</span></span>
<span data-ttu-id="081d0-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081d0-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081d0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081d0-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="081d0-136">INPUTS</span></span>

### <span data-ttu-id="081d0-137">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="081d0-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="081d0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="081d0-138">System.String</span></span>

## <span data-ttu-id="081d0-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="081d0-139">OUTPUTS</span></span>

### <span data-ttu-id="081d0-140">System. void</span><span class="sxs-lookup"><span data-stu-id="081d0-140">System.Void</span></span>

## <span data-ttu-id="081d0-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="081d0-141">NOTES</span></span>

## <span data-ttu-id="081d0-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="081d0-142">RELATED LINKS</span></span>

[<span data-ttu-id="081d0-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="081d0-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="081d0-144">Rejestr — AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="081d0-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)



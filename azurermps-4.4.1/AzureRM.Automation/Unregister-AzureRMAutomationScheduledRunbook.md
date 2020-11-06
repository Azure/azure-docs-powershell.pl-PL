---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: aa970f71be1e80f9eb5fcc1b4ec24cf0ce7f0e9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552423"
---
# <span data-ttu-id="e2870-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e2870-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="e2870-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2870-102">SYNOPSIS</span></span>
<span data-ttu-id="e2870-103">Usuwa skojarzenie między elementem Runbook a harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="e2870-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2870-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2870-104">SYNTAX</span></span>

### <span data-ttu-id="e2870-105">ByJobScheduleId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e2870-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2870-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="e2870-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2870-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e2870-107">DESCRIPTION</span></span>
<span data-ttu-id="e2870-108">Polecenie cmdlet **Unregister-AzureRmAutomationScheduledRunbook** powoduje usunięcie skojarzenia elementu Runbook usługi Azure Automation i harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="e2870-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="e2870-109">Harmonogram nie będzie już uruchamiał elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e2870-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="e2870-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2870-110">EXAMPLES</span></span>

### <span data-ttu-id="e2870-111">Przykład 1: Usuwanie skojarzenia między elementem Runbook a harmonogramem</span><span class="sxs-lookup"><span data-stu-id="e2870-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="e2870-112">To polecenie powoduje usunięcie skojarzenia między elementem Runbook o nazwie Runbk01 a harmonogramem o nazwie Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="e2870-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="e2870-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2870-113">PARAMETERS</span></span>

### <span data-ttu-id="e2870-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e2870-114">-AutomationAccountName</span></span>
<span data-ttu-id="e2870-115">Określa konto usługi Automation dla elementu Runbook, dla którego działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2870-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e2870-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e2870-116">-Force</span></span>
<span data-ttu-id="e2870-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="e2870-117">ps_force</span></span>

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

### <span data-ttu-id="e2870-118">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="e2870-118">-JobScheduleId</span></span>
<span data-ttu-id="e2870-119">Określa identyfikator zaplanowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e2870-119">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="e2870-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2870-120">-ResourceGroupName</span></span>
<span data-ttu-id="e2870-121">Określa nazwę grupy zasobów dla zaplanowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e2870-121">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="e2870-122">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="e2870-122">-RunbookName</span></span>
<span data-ttu-id="e2870-123">Określa nazwę elementu Runbook, który jest niezgodny z harmonogramem tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2870-123">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="e2870-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="e2870-124">-ScheduleName</span></span>
<span data-ttu-id="e2870-125">Określa nazwę harmonogramu, z którego to polecenie cmdlet powoduje skojarzenie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e2870-125">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="e2870-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2870-126">-Confirm</span></span>
<span data-ttu-id="e2870-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2870-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2870-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2870-128">-WhatIf</span></span>
<span data-ttu-id="e2870-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2870-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2870-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2870-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2870-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2870-131">-DefaultProfile</span></span>
<span data-ttu-id="e2870-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2870-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2870-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2870-133">CommonParameters</span></span>
<span data-ttu-id="e2870-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2870-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2870-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2870-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2870-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2870-136">INPUTS</span></span>

## <span data-ttu-id="e2870-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2870-137">OUTPUTS</span></span>

## <span data-ttu-id="e2870-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2870-138">NOTES</span></span>

## <span data-ttu-id="e2870-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2870-139">RELATED LINKS</span></span>

[<span data-ttu-id="e2870-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e2870-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="e2870-141">Rejestr — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e2870-141">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)



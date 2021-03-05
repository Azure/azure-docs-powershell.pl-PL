---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: a7dc06e4ddbeac224daf9b8a80be40d343514a18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009889"
---
# <span data-ttu-id="08e97-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="08e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08e97-102">SYNOPSIS</span></span>
<span data-ttu-id="08e97-103">Usuwa podręcznik.</span><span class="sxs-lookup"><span data-stu-id="08e97-103">Removes a runbook.</span></span>

## <span data-ttu-id="08e97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="08e97-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08e97-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="08e97-105">DESCRIPTION</span></span>
<span data-ttu-id="08e97-106">Polecenie **cmdlet Remove-AzAutomationRunbook** usuwa podręcznik z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="08e97-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="08e97-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="08e97-107">EXAMPLES</span></span>

### <span data-ttu-id="08e97-108">Przykład 1. Usuwanie podręcznika</span><span class="sxs-lookup"><span data-stu-id="08e97-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="08e97-109">To polecenie usuwa podręcznik Runbook03 z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="08e97-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="08e97-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08e97-110">PARAMETERS</span></span>

### <span data-ttu-id="08e97-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08e97-111">-AutomationAccountName</span></span>
<span data-ttu-id="08e97-112">Określa nazwę konta automatyzacji, z którego to polecenie cmdlet usuwa zestaw runbook.</span><span class="sxs-lookup"><span data-stu-id="08e97-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="08e97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e97-113">-DefaultProfile</span></span>
<span data-ttu-id="08e97-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="08e97-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08e97-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="08e97-115">-Force</span></span>
<span data-ttu-id="08e97-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="08e97-116">ps_force</span></span>

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

### <span data-ttu-id="08e97-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="08e97-117">-Name</span></span>
<span data-ttu-id="08e97-118">Określa nazwę zestawu runbook, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e97-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e97-119">-ResourceGroupName</span></span>
<span data-ttu-id="08e97-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet publikuje podręcznik.</span><span class="sxs-lookup"><span data-stu-id="08e97-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="08e97-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08e97-121">-Confirm</span></span>
<span data-ttu-id="08e97-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="08e97-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08e97-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08e97-123">-WhatIf</span></span>
<span data-ttu-id="08e97-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e97-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08e97-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="08e97-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08e97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e97-126">CommonParameters</span></span>
<span data-ttu-id="08e97-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e97-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e97-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e97-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08e97-129">INPUTS</span></span>

### <span data-ttu-id="08e97-130">System.String</span><span class="sxs-lookup"><span data-stu-id="08e97-130">System.String</span></span>

## <span data-ttu-id="08e97-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08e97-131">OUTPUTS</span></span>

### <span data-ttu-id="08e97-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="08e97-132">System.Void</span></span>

## <span data-ttu-id="08e97-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="08e97-133">NOTES</span></span>

## <span data-ttu-id="08e97-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08e97-134">RELATED LINKS</span></span>

[<span data-ttu-id="08e97-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="08e97-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="08e97-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="08e97-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="08e97-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="08e97-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="08e97-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="08e97-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08e97-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



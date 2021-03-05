---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 38e993068bec6e4a2fd8e627ed7201fb0f966633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014314"
---
# <span data-ttu-id="97190-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="97190-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97190-102">SYNOPSIS</span></span>
<span data-ttu-id="97190-103">Eksportuje podręcznik automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="97190-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="97190-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97190-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97190-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="97190-105">DESCRIPTION</span></span>
<span data-ttu-id="97190-106">Polecenie cmdlet **Export-AzAutomationRunbook** eksportuje runbook azure automation do pliku skryptu programu wps_2 (ps1), wps_2 lub wps_2 Runbooks przepływu pracy lub do pliku graficznego runbooka (graphrunbook) dla graficznych runbooków.</span><span class="sxs-lookup"><span data-stu-id="97190-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="97190-107">Nazwa podręcznika stanie się nazwą wyeksportowanego pliku.</span><span class="sxs-lookup"><span data-stu-id="97190-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="97190-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97190-108">EXAMPLES</span></span>

### <span data-ttu-id="97190-109">Przykład 1. Eksportowanie podręcznika</span><span class="sxs-lookup"><span data-stu-id="97190-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="97190-110">To polecenie eksportuje opublikowaną wersję podręcznika uruchamiania automatyzacji do pulpitu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="97190-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="97190-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97190-111">PARAMETERS</span></span>

### <span data-ttu-id="97190-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97190-112">-AutomationAccountName</span></span>
<span data-ttu-id="97190-113">Określa nazwę konta automatyzacji, z którego to polecenie cmdlet eksportuje zestaw runbook.</span><span class="sxs-lookup"><span data-stu-id="97190-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="97190-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97190-114">-DefaultProfile</span></span>
<span data-ttu-id="97190-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="97190-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97190-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="97190-116">-Force</span></span>
<span data-ttu-id="97190-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="97190-117">ps_force</span></span>

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

### <span data-ttu-id="97190-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="97190-118">-Name</span></span>
<span data-ttu-id="97190-119">Określa nazwę podręcznika, który eksportuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97190-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="97190-120">Nazwa podręcznika stanie się nazwą pliku eksportu.</span><span class="sxs-lookup"><span data-stu-id="97190-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="97190-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="97190-121">-OutputFolder</span></span>
<span data-ttu-id="97190-122">Określa ścieżkę folderu, w którym to polecenie cmdlet tworzy plik eksportu.</span><span class="sxs-lookup"><span data-stu-id="97190-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97190-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97190-123">-ResourceGroupName</span></span>
<span data-ttu-id="97190-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet eksportuje zestaw runbook.</span><span class="sxs-lookup"><span data-stu-id="97190-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="97190-125">— Slot</span><span class="sxs-lookup"><span data-stu-id="97190-125">-Slot</span></span>
<span data-ttu-id="97190-126">Określa, czy to polecenie cmdlet eksportuje zawartość roboczą, czy opublikowaną podręcznika.</span><span class="sxs-lookup"><span data-stu-id="97190-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="97190-127">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="97190-127">Valid values are:</span></span> 
- <span data-ttu-id="97190-128">Opublikowano</span><span class="sxs-lookup"><span data-stu-id="97190-128">Published</span></span> 
- <span data-ttu-id="97190-129">Wersja robocza</span><span class="sxs-lookup"><span data-stu-id="97190-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97190-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97190-130">-Confirm</span></span>
<span data-ttu-id="97190-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97190-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97190-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97190-132">-WhatIf</span></span>
<span data-ttu-id="97190-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97190-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97190-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="97190-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97190-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97190-135">CommonParameters</span></span>
<span data-ttu-id="97190-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97190-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97190-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97190-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97190-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97190-138">INPUTS</span></span>

### <span data-ttu-id="97190-139">System.String</span><span class="sxs-lookup"><span data-stu-id="97190-139">System.String</span></span>

## <span data-ttu-id="97190-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97190-140">OUTPUTS</span></span>

### <span data-ttu-id="97190-141">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="97190-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="97190-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97190-142">NOTES</span></span>

## <span data-ttu-id="97190-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97190-143">RELATED LINKS</span></span>

[<span data-ttu-id="97190-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="97190-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="97190-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="97190-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="97190-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="97190-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="97190-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="97190-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="97190-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 6d0af3f0d991d8d6b1f73c3277f9f86ac8dd0dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710611"
---
# <span data-ttu-id="2a6b3-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="2a6b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="2a6b3-103">Umożliwia wyeksportowanie elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="2a6b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a6b3-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a6b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="2a6b3-106">Polecenie cmdlet **Export-AzAutomationRunbook** eksportu element Runbook usługi Azure Automation do pliku skryptu wps_2 (. ps1), dla wps_2 lub wps_2 elementów Runbook przepływu pracy albo do graficznego pliku Runbook (graphrunbook) dla graficznych elementów Runbook.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="2a6b3-107">Nazwa elementu Runbook stanie się nazwą eksportowanego pliku.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="2a6b3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a6b3-108">EXAMPLES</span></span>

### <span data-ttu-id="2a6b3-109">Przykład 1: eksportowanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="2a6b3-110">To polecenie umożliwia wyeksportowanie opublikowanej wersji elementu Runbook usługi Automation na pulpit użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="2a6b3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a6b3-111">PARAMETERS</span></span>

### <span data-ttu-id="2a6b3-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2a6b3-112">-AutomationAccountName</span></span>
<span data-ttu-id="2a6b3-113">Określa nazwę konta automatyzacji, w którym ten polecenie cmdlet eksportuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="2a6b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a6b3-114">-DefaultProfile</span></span>
<span data-ttu-id="2a6b3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2a6b3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a6b3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2a6b3-116">-Force</span></span>
<span data-ttu-id="2a6b3-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="2a6b3-117">ps_force</span></span>

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

### <span data-ttu-id="2a6b3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a6b3-118">-Name</span></span>
<span data-ttu-id="2a6b3-119">Określa nazwę elementu Runbook wyeksportowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="2a6b3-120">Nazwa elementu Runbook stanie się nazwą pliku eksportu.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="2a6b3-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="2a6b3-121">-OutputFolder</span></span>
<span data-ttu-id="2a6b3-122">Określa ścieżkę do folderu, w którym ten polecenie cmdlet tworzy plik eksportu.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="2a6b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a6b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="2a6b3-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet eksportuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="2a6b3-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="2a6b3-125">-Slot</span></span>
<span data-ttu-id="2a6b3-126">Określa, czy to polecenie cmdlet eksportuje wersję roboczą lub opublikowaną elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="2a6b3-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="2a6b3-127">Valid values are:</span></span> 
- <span data-ttu-id="2a6b3-128">Podawane</span><span class="sxs-lookup"><span data-stu-id="2a6b3-128">Published</span></span> 
- <span data-ttu-id="2a6b3-129">Propozycje</span><span class="sxs-lookup"><span data-stu-id="2a6b3-129">Draft</span></span>

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

### <span data-ttu-id="2a6b3-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a6b3-130">-Confirm</span></span>
<span data-ttu-id="2a6b3-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a6b3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a6b3-132">-WhatIf</span></span>
<span data-ttu-id="2a6b3-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a6b3-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a6b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a6b3-135">CommonParameters</span></span>
<span data-ttu-id="2a6b3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a6b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a6b3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a6b3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a6b3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a6b3-138">INPUTS</span></span>

### <span data-ttu-id="2a6b3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2a6b3-139">System.String</span></span>

## <span data-ttu-id="2a6b3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a6b3-140">OUTPUTS</span></span>

### <span data-ttu-id="2a6b3-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="2a6b3-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="2a6b3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a6b3-142">NOTES</span></span>

## <span data-ttu-id="2a6b3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a6b3-143">RELATED LINKS</span></span>

[<span data-ttu-id="2a6b3-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="2a6b3-145">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="2a6b3-146">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="2a6b3-147">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="2a6b3-148">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="2a6b3-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="2a6b3-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="2a6b3-151">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a6b3-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



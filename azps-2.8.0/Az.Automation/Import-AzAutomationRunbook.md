---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: 9ec19ee8e1e6a74de83f77b8dca4e2536af8e425
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706774"
---
# <span data-ttu-id="1a4b4-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="1a4b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4b4-103">Import elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="1a4b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a4b4-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a4b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1a4b4-105">DESCRIPTION</span></span>
<span data-ttu-id="1a4b4-106">Polecenie cmdlet **Import-AzAutomationRunbook** importuje element Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="1a4b4-107">Określ ścieżkę do pliku skryptu wps_2 (. ps1), który ma zostać zaimportowany dla wps_2 i wps_2 elementów Runbook przepływu pracy, (graphrunbook) dla graficznych elementów Runbook lub pliku (. z) dla elementów Runbook języka Python 2.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="1a4b4-108">W przypadku elementów Runbook przepływu pracy wps_2 skrypt musi zawierać jedną definicję wps_2 przepływu pracy zgodną z nazwą pliku.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="1a4b4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a4b4-109">EXAMPLES</span></span>

### <span data-ttu-id="1a4b4-110">Przykład 1: Importowanie elementu Runbook z pliku</span><span class="sxs-lookup"><span data-stu-id="1a4b4-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="1a4b4-111">Pierwsze polecenie powoduje przypisanie dwóch par kluczy/wartości zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="1a4b4-112">Drugie polecenie importuje graficzny element Runbook o nazwie GraphicalRunbook06 do konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="1a4b4-113">Polecenie umożliwia także przypisanie znaczników przechowywanych w $Tags.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="1a4b4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a4b4-114">PARAMETERS</span></span>

### <span data-ttu-id="1a4b4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a4b4-115">-AutomationAccountName</span></span>
<span data-ttu-id="1a4b4-116">Określa nazwę konta automatyzacji, do którego zostanie zaimportowany element Runbook za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="1a4b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a4b4-117">-DefaultProfile</span></span>
<span data-ttu-id="1a4b4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1a4b4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a4b4-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="1a4b4-119">-Description</span></span>
<span data-ttu-id="1a4b4-120">Umożliwia określenie opisu zaimportowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="1a4b4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1a4b4-121">-Force</span></span>
<span data-ttu-id="1a4b4-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="1a4b4-122">ps_force</span></span>

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

### <span data-ttu-id="1a4b4-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="1a4b4-123">-LogProgress</span></span>
<span data-ttu-id="1a4b4-124">Określa, czy element Runbook rejestruje informacje o postępie.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4b4-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="1a4b4-125">-LogVerbose</span></span>
<span data-ttu-id="1a4b4-126">Określa, czy informacje szczegółowe są rejestrowane przez element Runbook.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4b4-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a4b4-127">-Name</span></span>
<span data-ttu-id="1a4b4-128">Określa nazwę elementu Runbook zaimportowanego za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4b4-129">-Path</span><span class="sxs-lookup"><span data-stu-id="1a4b4-129">-Path</span></span>
<span data-ttu-id="1a4b4-130">Określa ścieżkę pliku PS1 lub graphrunbook, który został zaimportowany za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4b4-131">-Opublikowano</span><span class="sxs-lookup"><span data-stu-id="1a4b4-131">-Published</span></span>
<span data-ttu-id="1a4b4-132">Wskazuje, że to polecenie cmdlet publikuje element Runbook, który został przez niego zaimportowany.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="1a4b4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a4b4-133">-ResourceGroupName</span></span>
<span data-ttu-id="1a4b4-134">Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="1a4b4-135">-Tagi</span><span class="sxs-lookup"><span data-stu-id="1a4b4-135">-Tags</span></span>
<span data-ttu-id="1a4b4-136">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1a4b4-137">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1a4b4-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4b4-138">-Type</span><span class="sxs-lookup"><span data-stu-id="1a4b4-138">-Type</span></span>
<span data-ttu-id="1a4b4-139">Określa typ elementu Runbook tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="1a4b4-140">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="1a4b4-140">Valid values are:</span></span>
- <span data-ttu-id="1a4b4-141">Narzędzia</span><span class="sxs-lookup"><span data-stu-id="1a4b4-141">PowerShell</span></span>
- <span data-ttu-id="1a4b4-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="1a4b4-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="1a4b4-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="1a4b4-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="1a4b4-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="1a4b4-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="1a4b4-145">Graf</span><span class="sxs-lookup"><span data-stu-id="1a4b4-145">Graph</span></span>
- <span data-ttu-id="1a4b4-146">Python2 wykres wartości jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="1a4b4-147">Jest to równoznaczne z GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a4b4-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a4b4-148">-Confirm</span></span>
<span data-ttu-id="1a4b4-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a4b4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a4b4-150">-WhatIf</span></span>
<span data-ttu-id="1a4b4-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a4b4-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a4b4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4b4-153">CommonParameters</span></span>
<span data-ttu-id="1a4b4-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a4b4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4b4-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a4b4-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4b4-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a4b4-156">INPUTS</span></span>

### <span data-ttu-id="1a4b4-157">System. String</span><span class="sxs-lookup"><span data-stu-id="1a4b4-157">System.String</span></span>

### <span data-ttu-id="1a4b4-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="1a4b4-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="1a4b4-159">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1a4b4-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1a4b4-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a4b4-160">OUTPUTS</span></span>

### <span data-ttu-id="1a4b4-161">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="1a4b4-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a4b4-162">NOTES</span></span>

## <span data-ttu-id="1a4b4-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a4b4-163">RELATED LINKS</span></span>

[<span data-ttu-id="1a4b4-164">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="1a4b4-165">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="1a4b4-166">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1a4b4-167">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-167">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="1a4b4-168">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-168">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="1a4b4-169">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-169">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="1a4b4-170">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1a4b4-170">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

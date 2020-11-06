---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: f6399c35316deb5590eada9eccd474ba7e47b116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547663"
---
# <span data-ttu-id="96e3b-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="96e3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="96e3b-103">Import elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="96e3b-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96e3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96e3b-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96e3b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="96e3b-105">DESCRIPTION</span></span>
<span data-ttu-id="96e3b-106">Polecenie cmdlet **Import-AzureRmAutomationRunbook** importuje element Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="96e3b-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="96e3b-107">Określ ścieżkę do pliku skryptu wps_2 (. ps1), który ma zostać zaimportowany dla wps_2 i wps_2 elementów Runbook przepływu pracy, (graphrunbook) dla graficznych elementów Runbook lub pliku (. z) dla elementów Runbook języka Python 2.</span><span class="sxs-lookup"><span data-stu-id="96e3b-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="96e3b-108">W przypadku elementów Runbook przepływu pracy wps_2 skrypt musi zawierać jedną definicję wps_2 przepływu pracy zgodną z nazwą pliku.</span><span class="sxs-lookup"><span data-stu-id="96e3b-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="96e3b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96e3b-109">EXAMPLES</span></span>

### <span data-ttu-id="96e3b-110">Przykład 1: Importowanie elementu Runbook z pliku</span><span class="sxs-lookup"><span data-stu-id="96e3b-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="96e3b-111">Pierwsze polecenie powoduje przypisanie dwóch par kluczy/wartości zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="96e3b-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="96e3b-112">Drugie polecenie importuje graficzny element Runbook o nazwie GraphicalRunbook06 do konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="96e3b-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="96e3b-113">Polecenie umożliwia także przypisanie znaczników przechowywanych w $Tags.</span><span class="sxs-lookup"><span data-stu-id="96e3b-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="96e3b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96e3b-114">PARAMETERS</span></span>

### <span data-ttu-id="96e3b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="96e3b-115">-AutomationAccountName</span></span>
<span data-ttu-id="96e3b-116">Określa nazwę konta automatyzacji, do którego zostanie zaimportowany element Runbook za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e3b-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="96e3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e3b-117">-DefaultProfile</span></span>
<span data-ttu-id="96e3b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="96e3b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96e3b-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="96e3b-119">-Description</span></span>
<span data-ttu-id="96e3b-120">Umożliwia określenie opisu zaimportowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="96e3b-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="96e3b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="96e3b-121">-Force</span></span>
<span data-ttu-id="96e3b-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="96e3b-122">ps_force</span></span>

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

### <span data-ttu-id="96e3b-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="96e3b-123">-LogProgress</span></span>
<span data-ttu-id="96e3b-124">Określa, czy element Runbook rejestruje informacje o postępie.</span><span class="sxs-lookup"><span data-stu-id="96e3b-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="96e3b-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="96e3b-125">-LogVerbose</span></span>
<span data-ttu-id="96e3b-126">Określa, czy informacje szczegółowe są rejestrowane przez element Runbook.</span><span class="sxs-lookup"><span data-stu-id="96e3b-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="96e3b-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="96e3b-127">-Name</span></span>
<span data-ttu-id="96e3b-128">Określa nazwę elementu Runbook zaimportowanego za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e3b-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="96e3b-129">-Path</span><span class="sxs-lookup"><span data-stu-id="96e3b-129">-Path</span></span>
<span data-ttu-id="96e3b-130">Określa ścieżkę pliku PS1 lub graphrunbook, który został zaimportowany za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e3b-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="96e3b-131">-Opublikowano</span><span class="sxs-lookup"><span data-stu-id="96e3b-131">-Published</span></span>
<span data-ttu-id="96e3b-132">Wskazuje, że to polecenie cmdlet publikuje element Runbook, który został przez niego zaimportowany.</span><span class="sxs-lookup"><span data-stu-id="96e3b-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="96e3b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e3b-133">-ResourceGroupName</span></span>
<span data-ttu-id="96e3b-134">Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="96e3b-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="96e3b-135">-Tagi</span><span class="sxs-lookup"><span data-stu-id="96e3b-135">-Tags</span></span>
<span data-ttu-id="96e3b-136">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="96e3b-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="96e3b-137">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="96e3b-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="96e3b-138">-Type</span><span class="sxs-lookup"><span data-stu-id="96e3b-138">-Type</span></span>
<span data-ttu-id="96e3b-139">Określa typ elementu Runbook tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e3b-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="96e3b-140">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="96e3b-140">Valid values are:</span></span>
- <span data-ttu-id="96e3b-141">Narzędzia</span><span class="sxs-lookup"><span data-stu-id="96e3b-141">PowerShell</span></span>
- <span data-ttu-id="96e3b-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="96e3b-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="96e3b-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="96e3b-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="96e3b-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="96e3b-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="96e3b-145">Graf</span><span class="sxs-lookup"><span data-stu-id="96e3b-145">Graph</span></span>
- <span data-ttu-id="96e3b-146">Python2 wykres wartości jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="96e3b-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="96e3b-147">Jest to równoznaczne z GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="96e3b-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="96e3b-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96e3b-148">-Confirm</span></span>
<span data-ttu-id="96e3b-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e3b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e3b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e3b-150">-WhatIf</span></span>
<span data-ttu-id="96e3b-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e3b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96e3b-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96e3b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e3b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e3b-153">CommonParameters</span></span>
<span data-ttu-id="96e3b-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e3b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e3b-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e3b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e3b-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96e3b-156">INPUTS</span></span>

### <span data-ttu-id="96e3b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="96e3b-157">System.String</span></span>

### <span data-ttu-id="96e3b-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="96e3b-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="96e3b-159">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="96e3b-159">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="96e3b-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96e3b-160">OUTPUTS</span></span>

### <span data-ttu-id="96e3b-161">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="96e3b-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96e3b-162">NOTES</span></span>

## <span data-ttu-id="96e3b-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96e3b-163">RELATED LINKS</span></span>

[<span data-ttu-id="96e3b-164">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-164">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="96e3b-165">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-165">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="96e3b-166">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="96e3b-167">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="96e3b-168">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-168">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="96e3b-169">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-169">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="96e3b-170">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-170">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="96e3b-171">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="96e3b-171">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

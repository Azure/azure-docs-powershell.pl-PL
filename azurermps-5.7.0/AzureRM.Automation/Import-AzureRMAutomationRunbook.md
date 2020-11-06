---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1f7c50f0f5b11c80fce203b0c44128e380834bdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525370"
---
# <span data-ttu-id="5f4db-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="5f4db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f4db-102">SYNOPSIS</span></span>
<span data-ttu-id="5f4db-103">Import elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5f4db-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f4db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f4db-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f4db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f4db-105">DESCRIPTION</span></span>
<span data-ttu-id="5f4db-106">Polecenie cmdlet **Import-AzureRmAutomationRunbook** importuje element Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5f4db-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="5f4db-107">Określ ścieżkę do pliku skryptu wps_2 (. ps1), który ma zostać zaimportowany dla wps_2 i wps_2 elementów Runbook przepływu pracy, (graphrunbook) dla graficznych elementów Runbook lub pliku (. z) dla elementów Runbook języka Python 2.</span><span class="sxs-lookup"><span data-stu-id="5f4db-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="5f4db-108">W przypadku elementów Runbook przepływu pracy wps_2 skrypt musi zawierać jedną definicję wps_2 przepływu pracy zgodną z nazwą pliku.</span><span class="sxs-lookup"><span data-stu-id="5f4db-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="5f4db-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f4db-109">EXAMPLES</span></span>

### <span data-ttu-id="5f4db-110">Przykład 1: Importowanie elementu Runbook z pliku</span><span class="sxs-lookup"><span data-stu-id="5f4db-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="5f4db-111">Pierwsze polecenie powoduje przypisanie dwóch par kluczy/wartości zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="5f4db-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="5f4db-112">Drugie polecenie importuje graficzny element Runbook o nazwie GraphicalRunbook06 do konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="5f4db-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="5f4db-113">Polecenie umożliwia także przypisanie znaczników przechowywanych w $Tags.</span><span class="sxs-lookup"><span data-stu-id="5f4db-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="5f4db-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f4db-114">PARAMETERS</span></span>

### <span data-ttu-id="5f4db-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f4db-115">-AutomationAccountName</span></span>
<span data-ttu-id="5f4db-116">Określa nazwę konta automatyzacji, do którego zostanie zaimportowany element Runbook za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f4db-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f4db-117">-DefaultProfile</span></span>
<span data-ttu-id="5f4db-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5f4db-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="5f4db-119">-Description</span></span>
<span data-ttu-id="5f4db-120">Umożliwia określenie opisu zaimportowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="5f4db-120">Specifies a description for the imported runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5f4db-121">-Force</span></span>
<span data-ttu-id="5f4db-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="5f4db-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="5f4db-123">-LogProgress</span></span>
<span data-ttu-id="5f4db-124">Określa, czy element Runbook rejestruje informacje o postępie.</span><span class="sxs-lookup"><span data-stu-id="5f4db-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="5f4db-125">-LogVerbose</span></span>
<span data-ttu-id="5f4db-126">Określa, czy informacje szczegółowe są rejestrowane przez element Runbook.</span><span class="sxs-lookup"><span data-stu-id="5f4db-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f4db-127">-Name</span></span>
<span data-ttu-id="5f4db-128">Określa nazwę elementu Runbook zaimportowanego za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f4db-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-129">-Path</span><span class="sxs-lookup"><span data-stu-id="5f4db-129">-Path</span></span>
<span data-ttu-id="5f4db-130">Określa ścieżkę pliku PS1 lub graphrunbook, który został zaimportowany za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f4db-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-131">-Opublikowano</span><span class="sxs-lookup"><span data-stu-id="5f4db-131">-Published</span></span>
<span data-ttu-id="5f4db-132">Wskazuje, że to polecenie cmdlet publikuje element Runbook, który został przez niego zaimportowany.</span><span class="sxs-lookup"><span data-stu-id="5f4db-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f4db-133">-ResourceGroupName</span></span>
<span data-ttu-id="5f4db-134">Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="5f4db-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-135">-Tagi</span><span class="sxs-lookup"><span data-stu-id="5f4db-135">-Tags</span></span>
<span data-ttu-id="5f4db-136">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5f4db-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5f4db-137">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="5f4db-137">For example:</span></span>

<span data-ttu-id="5f4db-138">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5f4db-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-139">-Type</span><span class="sxs-lookup"><span data-stu-id="5f4db-139">-Type</span></span>
<span data-ttu-id="5f4db-140">Określa typ elementu Runbook tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f4db-140">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="5f4db-141">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="5f4db-141">Valid values are:</span></span>

- <span data-ttu-id="5f4db-142">Narzędzia</span><span class="sxs-lookup"><span data-stu-id="5f4db-142">PowerShell</span></span>
- <span data-ttu-id="5f4db-143">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="5f4db-143">GraphicalPowerShell</span></span>
- <span data-ttu-id="5f4db-144">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="5f4db-144">PowerShellWorkflow</span></span>
- <span data-ttu-id="5f4db-145">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="5f4db-145">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="5f4db-146">Graf</span><span class="sxs-lookup"><span data-stu-id="5f4db-146">Graph</span></span>
- <span data-ttu-id="5f4db-147">Python2</span><span class="sxs-lookup"><span data-stu-id="5f4db-147">Python2</span></span>

<span data-ttu-id="5f4db-148">Wykres wartości jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="5f4db-148">The value Graph is obsolete.</span></span>
<span data-ttu-id="5f4db-149">Jest to równoznaczne z GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="5f4db-149">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f4db-150">-Confirm</span></span>
<span data-ttu-id="5f4db-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f4db-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f4db-152">-WhatIf</span></span>
<span data-ttu-id="5f4db-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f4db-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f4db-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f4db-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4db-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f4db-155">CommonParameters</span></span>
<span data-ttu-id="5f4db-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f4db-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f4db-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f4db-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f4db-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f4db-158">INPUTS</span></span>

### <span data-ttu-id="5f4db-159">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5f4db-159">None</span></span>
<span data-ttu-id="5f4db-160">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5f4db-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f4db-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f4db-161">OUTPUTS</span></span>

### <span data-ttu-id="5f4db-162">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-162">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="5f4db-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f4db-163">NOTES</span></span>

## <span data-ttu-id="5f4db-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f4db-164">RELATED LINKS</span></span>

[<span data-ttu-id="5f4db-165">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-165">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f4db-166">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-166">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f4db-167">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f4db-168">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-168">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f4db-169">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-169">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f4db-170">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-170">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f4db-171">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-171">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f4db-172">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f4db-172">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

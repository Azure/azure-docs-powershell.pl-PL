---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547128"
---
# <span data-ttu-id="ed5b5-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="ed5b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5b5-103">Import elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed5b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed5b5-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed5b5-105">DESCRIPTION</span></span>
<span data-ttu-id="ed5b5-106">Polecenie cmdlet **Import-AzureRmAutomationRunbook** importuje element Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="ed5b5-107">Określ ścieżkę do pliku skryptu wps_2 (. ps1) do zaimportowania dla wps_2 i wps_2 elementów Runbook przepływu pracy albo do graficznego pliku elementu Runbook (. graphrunbook) dla graficznych elementów Runbook.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-107">Specify the path to a wps_2 script (.ps1 ) file to import for wps_2 and wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file for graphical runbooks.</span></span> <span data-ttu-id="ed5b5-108">Nazwa pliku staje się nazwą elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-108">The name of the file becomes the name of the runbook.</span></span> <span data-ttu-id="ed5b5-109">W przypadku elementów Runbook przepływu pracy wps_2 skrypt musi zawierać jedną definicję wps_2 przepływu pracy zgodną z nazwą pliku.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-109">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="ed5b5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed5b5-110">EXAMPLES</span></span>

### <span data-ttu-id="ed5b5-111">Przykład 1: Importowanie elementu Runbook z pliku</span><span class="sxs-lookup"><span data-stu-id="ed5b5-111">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="ed5b5-112">Pierwsze polecenie powoduje przypisanie dwóch par kluczy/wartości zmiennej $Tags.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-112">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="ed5b5-113">Drugie polecenie importuje graficzny element Runbook o nazwie GraphicalRunbook06 do konta usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-113">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="ed5b5-114">Polecenie umożliwia także przypisanie znaczników przechowywanych w $Tags.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-114">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="ed5b5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed5b5-115">PARAMETERS</span></span>

### <span data-ttu-id="ed5b5-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed5b5-116">-AutomationAccountName</span></span>
<span data-ttu-id="ed5b5-117">Określa nazwę konta automatyzacji, do którego zostanie zaimportowany element Runbook za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-117">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="ed5b5-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="ed5b5-118">-Description</span></span>
<span data-ttu-id="ed5b5-119">Umożliwia określenie opisu zaimportowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-119">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="ed5b5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ed5b5-120">-Force</span></span>
<span data-ttu-id="ed5b5-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="ed5b5-121">ps_force</span></span>

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

### <span data-ttu-id="ed5b5-122">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="ed5b5-122">-LogProgress</span></span>
<span data-ttu-id="ed5b5-123">Określa, czy element Runbook rejestruje informacje o postępie.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-123">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="ed5b5-124">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="ed5b5-124">-LogVerbose</span></span>
<span data-ttu-id="ed5b5-125">Określa, czy informacje szczegółowe są rejestrowane przez element Runbook.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-125">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="ed5b5-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed5b5-126">-Name</span></span>
<span data-ttu-id="ed5b5-127">Określa nazwę elementu Runbook zaimportowanego za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-127">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="ed5b5-128">-Path</span><span class="sxs-lookup"><span data-stu-id="ed5b5-128">-Path</span></span>
<span data-ttu-id="ed5b5-129">Określa ścieżkę pliku PS1 lub graphrunbook, który został zaimportowany za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-129">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="ed5b5-130">-Opublikowano</span><span class="sxs-lookup"><span data-stu-id="ed5b5-130">-Published</span></span>
<span data-ttu-id="ed5b5-131">Wskazuje, że to polecenie cmdlet publikuje element Runbook, który został przez niego zaimportowany.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-131">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="ed5b5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5b5-132">-ResourceGroupName</span></span>
<span data-ttu-id="ed5b5-133">Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-133">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="ed5b5-134">-Tagi</span><span class="sxs-lookup"><span data-stu-id="ed5b5-134">-Tags</span></span>
<span data-ttu-id="ed5b5-135">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ed5b5-136">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="ed5b5-136">For example:</span></span>

<span data-ttu-id="ed5b5-137">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ed5b5-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ed5b5-138">-Type</span><span class="sxs-lookup"><span data-stu-id="ed5b5-138">-Type</span></span>
<span data-ttu-id="ed5b5-139">Określa typ elementu Runbook tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="ed5b5-140">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ed5b5-140">Valid values are:</span></span>

- <span data-ttu-id="ed5b5-141">Narzędzia</span><span class="sxs-lookup"><span data-stu-id="ed5b5-141">PowerShell</span></span>
- <span data-ttu-id="ed5b5-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="ed5b5-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="ed5b5-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="ed5b5-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="ed5b5-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="ed5b5-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="ed5b5-145">Graf</span><span class="sxs-lookup"><span data-stu-id="ed5b5-145">Graph</span></span>

<span data-ttu-id="ed5b5-146">Wykres wartości jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-146">The value Graph is obsolete.</span></span>
<span data-ttu-id="ed5b5-147">Jest to równoznaczne z GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5b5-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed5b5-148">-Confirm</span></span>
<span data-ttu-id="ed5b5-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5b5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5b5-150">-WhatIf</span></span>
<span data-ttu-id="ed5b5-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5b5-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5b5-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5b5-153">-DefaultProfile</span></span>
<span data-ttu-id="ed5b5-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed5b5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5b5-155">CommonParameters</span></span>
<span data-ttu-id="ed5b5-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5b5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5b5-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed5b5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5b5-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed5b5-158">INPUTS</span></span>

## <span data-ttu-id="ed5b5-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed5b5-159">OUTPUTS</span></span>

### <span data-ttu-id="ed5b5-160">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-160">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ed5b5-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed5b5-161">NOTES</span></span>

## <span data-ttu-id="ed5b5-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed5b5-162">RELATED LINKS</span></span>

[<span data-ttu-id="ed5b5-163">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-163">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ed5b5-164">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-164">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ed5b5-165">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-165">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ed5b5-166">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ed5b5-167">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-167">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ed5b5-168">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-168">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ed5b5-169">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-169">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ed5b5-170">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ed5b5-170">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

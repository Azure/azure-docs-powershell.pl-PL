---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: f982c68c49d6a8a92bb06bf150e352626730f67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543971"
---
# <span data-ttu-id="d4068-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="d4068-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4068-102">SYNOPSIS</span></span>
<span data-ttu-id="d4068-103">Umożliwia wyeksportowanie elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d4068-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4068-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4068-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4068-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d4068-105">DESCRIPTION</span></span>
<span data-ttu-id="d4068-106">Polecenie cmdlet **Export-AzureRmAutomationRunbook** eksportu element Runbook usługi Azure Automation do pliku skryptu wps_2 (. ps1), dla wps_2 lub wps_2 elementów Runbook przepływu pracy albo do graficznego pliku Runbook (graphrunbook) dla graficznych elementów Runbook.</span><span class="sxs-lookup"><span data-stu-id="d4068-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="d4068-107">Nazwa elementu Runbook stanie się nazwą eksportowanego pliku.</span><span class="sxs-lookup"><span data-stu-id="d4068-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="d4068-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4068-108">EXAMPLES</span></span>

### <span data-ttu-id="d4068-109">Przykład 1: eksportowanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="d4068-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="d4068-110">To polecenie umożliwia wyeksportowanie opublikowanej wersji elementu Runbook usługi Automation na pulpit użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d4068-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="d4068-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4068-111">PARAMETERS</span></span>

### <span data-ttu-id="d4068-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d4068-112">-AutomationAccountName</span></span>
<span data-ttu-id="d4068-113">Określa nazwę konta automatyzacji, w którym ten polecenie cmdlet eksportuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="d4068-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="d4068-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4068-114">-DefaultProfile</span></span>
<span data-ttu-id="d4068-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d4068-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4068-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d4068-116">-Force</span></span>
<span data-ttu-id="d4068-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="d4068-117">ps_force</span></span>

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

### <span data-ttu-id="d4068-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4068-118">-Name</span></span>
<span data-ttu-id="d4068-119">Określa nazwę elementu Runbook wyeksportowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4068-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="d4068-120">Nazwa elementu Runbook stanie się nazwą pliku eksportu.</span><span class="sxs-lookup"><span data-stu-id="d4068-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="d4068-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="d4068-121">-OutputFolder</span></span>
<span data-ttu-id="d4068-122">Określa ścieżkę do folderu, w którym ten polecenie cmdlet tworzy plik eksportu.</span><span class="sxs-lookup"><span data-stu-id="d4068-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="d4068-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4068-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4068-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet eksportuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="d4068-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="d4068-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="d4068-125">-Slot</span></span>
<span data-ttu-id="d4068-126">Określa, czy to polecenie cmdlet eksportuje wersję roboczą lub opublikowaną elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="d4068-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="d4068-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d4068-127">Valid values are:</span></span> 
- <span data-ttu-id="d4068-128">Podawane</span><span class="sxs-lookup"><span data-stu-id="d4068-128">Published</span></span> 
- <span data-ttu-id="d4068-129">Propozycje</span><span class="sxs-lookup"><span data-stu-id="d4068-129">Draft</span></span>

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

### <span data-ttu-id="d4068-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4068-130">-Confirm</span></span>
<span data-ttu-id="d4068-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4068-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4068-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4068-132">-WhatIf</span></span>
<span data-ttu-id="d4068-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4068-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4068-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4068-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4068-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4068-135">CommonParameters</span></span>
<span data-ttu-id="d4068-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4068-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4068-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4068-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4068-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4068-138">INPUTS</span></span>

### <span data-ttu-id="d4068-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d4068-139">System.String</span></span>

## <span data-ttu-id="d4068-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4068-140">OUTPUTS</span></span>

### <span data-ttu-id="d4068-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="d4068-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="d4068-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4068-142">NOTES</span></span>

## <span data-ttu-id="d4068-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4068-143">RELATED LINKS</span></span>

[<span data-ttu-id="d4068-144">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-144">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d4068-145">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-145">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d4068-146">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d4068-147">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d4068-148">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-148">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d4068-149">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-149">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d4068-150">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-150">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d4068-151">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d4068-151">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)



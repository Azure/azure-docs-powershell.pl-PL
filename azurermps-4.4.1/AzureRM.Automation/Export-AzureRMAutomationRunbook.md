---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: b78b992e74252f645faabcf284c817b1cb3c1d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525730"
---
# <span data-ttu-id="0f57f-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="0f57f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f57f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f57f-103">Umożliwia wyeksportowanie elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="0f57f-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f57f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f57f-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f57f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f57f-105">DESCRIPTION</span></span>
<span data-ttu-id="0f57f-106">Polecenie cmdlet **Export-AzureRmAutomationRunbook** eksportu element Runbook usługi Azure Automation do pliku skryptu wps_2 (. ps1), dla wps_2 lub wps_2 elementów Runbook przepływu pracy albo do graficznego pliku Runbook (graphrunbook) dla graficznych elementów Runbook.</span><span class="sxs-lookup"><span data-stu-id="0f57f-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="0f57f-107">Nazwa elementu Runbook stanie się nazwą eksportowanego pliku.</span><span class="sxs-lookup"><span data-stu-id="0f57f-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="0f57f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f57f-108">EXAMPLES</span></span>

### <span data-ttu-id="0f57f-109">Przykład 1: eksportowanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="0f57f-110">To polecenie umożliwia wyeksportowanie opublikowanej wersji elementu Runbook usługi Automation na pulpit użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0f57f-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="0f57f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f57f-111">PARAMETERS</span></span>

### <span data-ttu-id="0f57f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0f57f-112">-AutomationAccountName</span></span>
<span data-ttu-id="0f57f-113">Określa nazwę konta automatyzacji, w którym ten polecenie cmdlet eksportuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="0f57f-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="0f57f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0f57f-114">-Force</span></span>
<span data-ttu-id="0f57f-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="0f57f-115">ps_force</span></span>

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

### <span data-ttu-id="0f57f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f57f-116">-Name</span></span>
<span data-ttu-id="0f57f-117">Określa nazwę elementu Runbook wyeksportowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f57f-117">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="0f57f-118">Nazwa elementu Runbook stanie się nazwą pliku eksportu.</span><span class="sxs-lookup"><span data-stu-id="0f57f-118">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="0f57f-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="0f57f-119">-OutputFolder</span></span>
<span data-ttu-id="0f57f-120">Określa ścieżkę do folderu, w którym ten polecenie cmdlet tworzy plik eksportu.</span><span class="sxs-lookup"><span data-stu-id="0f57f-120">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="0f57f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f57f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f57f-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet eksportuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="0f57f-122">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="0f57f-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="0f57f-123">-Slot</span></span>
<span data-ttu-id="0f57f-124">Określa, czy to polecenie cmdlet eksportuje wersję roboczą lub opublikowaną elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="0f57f-124">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="0f57f-125">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="0f57f-125">Valid values are:</span></span> 

- <span data-ttu-id="0f57f-126">Podawane</span><span class="sxs-lookup"><span data-stu-id="0f57f-126">Published</span></span> 
- <span data-ttu-id="0f57f-127">Propozycje</span><span class="sxs-lookup"><span data-stu-id="0f57f-127">Draft</span></span>

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

### <span data-ttu-id="0f57f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f57f-128">-Confirm</span></span>
<span data-ttu-id="0f57f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f57f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f57f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f57f-130">-WhatIf</span></span>
<span data-ttu-id="0f57f-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f57f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f57f-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f57f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f57f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f57f-133">-DefaultProfile</span></span>
<span data-ttu-id="0f57f-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f57f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f57f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f57f-135">CommonParameters</span></span>
<span data-ttu-id="0f57f-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f57f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f57f-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f57f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f57f-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f57f-138">INPUTS</span></span>

## <span data-ttu-id="0f57f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f57f-139">OUTPUTS</span></span>

### <span data-ttu-id="0f57f-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="0f57f-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="0f57f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f57f-141">NOTES</span></span>

## <span data-ttu-id="0f57f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f57f-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f57f-143">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-143">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0f57f-144">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-144">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0f57f-145">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-145">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0f57f-146">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0f57f-147">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-147">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0f57f-148">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-148">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0f57f-149">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-149">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0f57f-150">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f57f-150">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: c77413f27bcde145334221465cbe792a5e1eaa5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710491"
---
# <span data-ttu-id="5da8a-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="5da8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5da8a-102">SYNOPSIS</span></span>
<span data-ttu-id="5da8a-103">Usuwa element Runbook.</span><span class="sxs-lookup"><span data-stu-id="5da8a-103">Removes a runbook.</span></span>

## <span data-ttu-id="5da8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5da8a-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5da8a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5da8a-105">DESCRIPTION</span></span>
<span data-ttu-id="5da8a-106">Polecenie cmdlet **Remove-AzAutomationRunbook** usuwa element Runbook z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5da8a-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="5da8a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5da8a-107">EXAMPLES</span></span>

### <span data-ttu-id="5da8a-108">Przykład 1. Usuń element Runbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5da8a-109">To polecenie usuwa element Runbook o nazwie Runbook03 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5da8a-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5da8a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5da8a-110">PARAMETERS</span></span>

### <span data-ttu-id="5da8a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5da8a-111">-AutomationAccountName</span></span>
<span data-ttu-id="5da8a-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet usuwa element Runbook.</span><span class="sxs-lookup"><span data-stu-id="5da8a-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="5da8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da8a-113">-DefaultProfile</span></span>
<span data-ttu-id="5da8a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5da8a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5da8a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5da8a-115">-Force</span></span>
<span data-ttu-id="5da8a-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="5da8a-116">ps_force</span></span>

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

### <span data-ttu-id="5da8a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5da8a-117">-Name</span></span>
<span data-ttu-id="5da8a-118">Określa nazwę elementu Runbook usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da8a-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5da8a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da8a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5da8a-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="5da8a-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="5da8a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5da8a-121">-Confirm</span></span>
<span data-ttu-id="5da8a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da8a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da8a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5da8a-123">-WhatIf</span></span>
<span data-ttu-id="5da8a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da8a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5da8a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5da8a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da8a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da8a-126">CommonParameters</span></span>
<span data-ttu-id="5da8a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da8a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da8a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da8a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da8a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5da8a-129">INPUTS</span></span>

### <span data-ttu-id="5da8a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5da8a-130">System.String</span></span>

## <span data-ttu-id="5da8a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5da8a-131">OUTPUTS</span></span>

### <span data-ttu-id="5da8a-132">System. void</span><span class="sxs-lookup"><span data-stu-id="5da8a-132">System.Void</span></span>

## <span data-ttu-id="5da8a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5da8a-133">NOTES</span></span>

## <span data-ttu-id="5da8a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5da8a-134">RELATED LINKS</span></span>

[<span data-ttu-id="5da8a-135">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="5da8a-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="5da8a-137">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="5da8a-138">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="5da8a-139">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="5da8a-140">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="5da8a-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="5da8a-142">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5da8a-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



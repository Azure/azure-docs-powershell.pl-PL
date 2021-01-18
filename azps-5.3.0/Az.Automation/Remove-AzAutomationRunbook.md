---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502282"
---
# <span data-ttu-id="75e32-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="75e32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75e32-102">SYNOPSIS</span></span>
<span data-ttu-id="75e32-103">Usuwa element Runbook.</span><span class="sxs-lookup"><span data-stu-id="75e32-103">Removes a runbook.</span></span>

## <span data-ttu-id="75e32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75e32-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75e32-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75e32-105">DESCRIPTION</span></span>
<span data-ttu-id="75e32-106">Polecenie cmdlet **Remove-AzAutomationRunbook** usuwa element Runbook z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="75e32-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="75e32-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75e32-107">EXAMPLES</span></span>

### <span data-ttu-id="75e32-108">Przykład 1. Usuń element Runbook</span><span class="sxs-lookup"><span data-stu-id="75e32-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="75e32-109">To polecenie usuwa element Runbook o nazwie Runbook03 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="75e32-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="75e32-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75e32-110">PARAMETERS</span></span>

### <span data-ttu-id="75e32-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="75e32-111">-AutomationAccountName</span></span>
<span data-ttu-id="75e32-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet usuwa element Runbook.</span><span class="sxs-lookup"><span data-stu-id="75e32-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="75e32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e32-113">-DefaultProfile</span></span>
<span data-ttu-id="75e32-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="75e32-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75e32-115">-Force</span><span class="sxs-lookup"><span data-stu-id="75e32-115">-Force</span></span>
<span data-ttu-id="75e32-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="75e32-116">ps_force</span></span>

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

### <span data-ttu-id="75e32-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75e32-117">-Name</span></span>
<span data-ttu-id="75e32-118">Określa nazwę elementu Runbook usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75e32-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="75e32-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e32-119">-ResourceGroupName</span></span>
<span data-ttu-id="75e32-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="75e32-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="75e32-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75e32-121">-Confirm</span></span>
<span data-ttu-id="75e32-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75e32-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75e32-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75e32-123">-WhatIf</span></span>
<span data-ttu-id="75e32-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75e32-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75e32-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="75e32-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75e32-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e32-126">CommonParameters</span></span>
<span data-ttu-id="75e32-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e32-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e32-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e32-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e32-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75e32-129">INPUTS</span></span>

### <span data-ttu-id="75e32-130">System. String</span><span class="sxs-lookup"><span data-stu-id="75e32-130">System.String</span></span>

## <span data-ttu-id="75e32-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75e32-131">OUTPUTS</span></span>

### <span data-ttu-id="75e32-132">System. void</span><span class="sxs-lookup"><span data-stu-id="75e32-132">System.Void</span></span>

## <span data-ttu-id="75e32-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75e32-133">NOTES</span></span>

## <span data-ttu-id="75e32-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75e32-134">RELATED LINKS</span></span>

[<span data-ttu-id="75e32-135">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="75e32-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="75e32-137">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="75e32-138">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="75e32-139">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="75e32-140">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="75e32-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="75e32-142">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="75e32-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



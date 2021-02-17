---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239499"
---
# <span data-ttu-id="4ee62-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4ee62-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="4ee62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee62-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee62-103">Usuwa webhook z podręcznika automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4ee62-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="4ee62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ee62-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee62-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ee62-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee62-106">Polecenie **cmdlet Remove-AzAutomationWebhook** usuwa webhook z podręcznika azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4ee62-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="4ee62-107">Webhook zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="4ee62-107">The webhook is deleted.</span></span>

## <span data-ttu-id="4ee62-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ee62-108">EXAMPLES</span></span>

### <span data-ttu-id="4ee62-109">Przykład 1. Usuwanie webhook</span><span class="sxs-lookup"><span data-stu-id="4ee62-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="4ee62-110">To polecenie usuwa webhook o nazwie Webhook11 z konta automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="4ee62-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="4ee62-111">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="4ee62-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4ee62-112">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ee62-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4ee62-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ee62-113">PARAMETERS</span></span>

### <span data-ttu-id="4ee62-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ee62-114">-AutomationAccountName</span></span>
<span data-ttu-id="4ee62-115">Określa nazwę konta automatyzacji, z którego to polecenie cmdlet usuwa webhook.</span><span class="sxs-lookup"><span data-stu-id="4ee62-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="4ee62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee62-116">-DefaultProfile</span></span>
<span data-ttu-id="4ee62-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4ee62-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ee62-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ee62-118">-Name</span></span>
<span data-ttu-id="4ee62-119">Określa nazwę sieci Web, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee62-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee62-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ee62-121">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usuwa webhook.</span><span class="sxs-lookup"><span data-stu-id="4ee62-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="4ee62-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ee62-122">-Confirm</span></span>
<span data-ttu-id="4ee62-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ee62-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee62-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee62-124">-WhatIf</span></span>
<span data-ttu-id="4ee62-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee62-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee62-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4ee62-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee62-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee62-127">CommonParameters</span></span>
<span data-ttu-id="4ee62-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee62-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee62-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee62-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee62-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ee62-130">INPUTS</span></span>

### <span data-ttu-id="4ee62-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4ee62-131">System.String</span></span>

## <span data-ttu-id="4ee62-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ee62-132">OUTPUTS</span></span>

### <span data-ttu-id="4ee62-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="4ee62-133">System.Void</span></span>

## <span data-ttu-id="4ee62-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ee62-134">NOTES</span></span>

## <span data-ttu-id="4ee62-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ee62-135">RELATED LINKS</span></span>

[<span data-ttu-id="4ee62-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4ee62-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="4ee62-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4ee62-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="4ee62-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4ee62-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



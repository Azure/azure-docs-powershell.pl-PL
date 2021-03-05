---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 93c370eaefa83c5e1be4692cb41ea0793b8f4681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009841"
---
# <span data-ttu-id="1ff4a-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1ff4a-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="1ff4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ff4a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff4a-103">Usuwa webhook z podręcznika automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="1ff4a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1ff4a-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ff4a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1ff4a-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff4a-106">Polecenie **cmdlet Remove-AzAutomationWebhook** usuwa webhook z podręcznika azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="1ff4a-107">Webhook zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-107">The webhook is deleted.</span></span>

## <span data-ttu-id="1ff4a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1ff4a-108">EXAMPLES</span></span>

### <span data-ttu-id="1ff4a-109">Przykład 1. Usuwanie webhook</span><span class="sxs-lookup"><span data-stu-id="1ff4a-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="1ff4a-110">To polecenie usuwa webhook o nazwie Webhook11 z konta automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="1ff4a-111">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="1ff4a-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1ff4a-112">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1ff4a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ff4a-113">PARAMETERS</span></span>

### <span data-ttu-id="1ff4a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ff4a-114">-AutomationAccountName</span></span>
<span data-ttu-id="1ff4a-115">Określa nazwę konta automatyzacji, z którego to polecenie cmdlet usuwa webhook.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="1ff4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff4a-116">-DefaultProfile</span></span>
<span data-ttu-id="1ff4a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1ff4a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ff4a-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1ff4a-118">-Name</span></span>
<span data-ttu-id="1ff4a-119">Określa nazwę sieci Web, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ff4a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff4a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1ff4a-121">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usuwa webhook.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="1ff4a-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ff4a-122">-Confirm</span></span>
<span data-ttu-id="1ff4a-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ff4a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff4a-124">-WhatIf</span></span>
<span data-ttu-id="1ff4a-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ff4a-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ff4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff4a-127">CommonParameters</span></span>
<span data-ttu-id="1ff4a-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff4a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ff4a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff4a-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ff4a-130">INPUTS</span></span>

### <span data-ttu-id="1ff4a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1ff4a-131">System.String</span></span>

## <span data-ttu-id="1ff4a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ff4a-132">OUTPUTS</span></span>

### <span data-ttu-id="1ff4a-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="1ff4a-133">System.Void</span></span>

## <span data-ttu-id="1ff4a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1ff4a-134">NOTES</span></span>

## <span data-ttu-id="1ff4a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ff4a-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ff4a-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1ff4a-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="1ff4a-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1ff4a-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="1ff4a-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1ff4a-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



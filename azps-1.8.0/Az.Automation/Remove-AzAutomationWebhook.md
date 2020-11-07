---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 5f3ba7d2bdc573e7a08976e575e86dcf05ae3400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710482"
---
# <span data-ttu-id="74e88-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="74e88-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="74e88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74e88-102">SYNOPSIS</span></span>
<span data-ttu-id="74e88-103">Usuwa element webhook z elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="74e88-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="74e88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74e88-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74e88-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74e88-105">DESCRIPTION</span></span>
<span data-ttu-id="74e88-106">Polecenie cmdlet **Remove-AzAutomationWebhook** usuwa element webhook z elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="74e88-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="74e88-107">Element webhook zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="74e88-107">The webhook is deleted.</span></span>

## <span data-ttu-id="74e88-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74e88-108">EXAMPLES</span></span>

### <span data-ttu-id="74e88-109">Przykład 1: usuwanie elementu webhook</span><span class="sxs-lookup"><span data-stu-id="74e88-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="74e88-110">To polecenie usuwa element webhook o nazwie Webhook11 na koncie automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="74e88-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="74e88-111">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="74e88-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="74e88-112">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74e88-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="74e88-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74e88-113">PARAMETERS</span></span>

### <span data-ttu-id="74e88-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="74e88-114">-AutomationAccountName</span></span>
<span data-ttu-id="74e88-115">Określa nazwę konta automatyzacji, na podstawie którego to polecenie cmdlet usuwa element webhook.</span><span class="sxs-lookup"><span data-stu-id="74e88-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="74e88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e88-116">-DefaultProfile</span></span>
<span data-ttu-id="74e88-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="74e88-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74e88-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74e88-118">-Name</span></span>
<span data-ttu-id="74e88-119">Określa nazwę elementu webhook, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74e88-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="74e88-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e88-120">-ResourceGroupName</span></span>
<span data-ttu-id="74e88-121">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie element webhook.</span><span class="sxs-lookup"><span data-stu-id="74e88-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="74e88-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74e88-122">-Confirm</span></span>
<span data-ttu-id="74e88-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74e88-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74e88-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74e88-124">-WhatIf</span></span>
<span data-ttu-id="74e88-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74e88-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74e88-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74e88-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74e88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e88-127">CommonParameters</span></span>
<span data-ttu-id="74e88-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74e88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e88-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e88-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e88-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74e88-130">INPUTS</span></span>

### <span data-ttu-id="74e88-131">System. String</span><span class="sxs-lookup"><span data-stu-id="74e88-131">System.String</span></span>

## <span data-ttu-id="74e88-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74e88-132">OUTPUTS</span></span>

### <span data-ttu-id="74e88-133">System. void</span><span class="sxs-lookup"><span data-stu-id="74e88-133">System.Void</span></span>

## <span data-ttu-id="74e88-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74e88-134">NOTES</span></span>

## <span data-ttu-id="74e88-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74e88-135">RELATED LINKS</span></span>

[<span data-ttu-id="74e88-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="74e88-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="74e88-137">Nowe — AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="74e88-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="74e88-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="74e88-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



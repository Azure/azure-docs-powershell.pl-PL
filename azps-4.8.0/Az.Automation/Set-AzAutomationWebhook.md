---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222686"
---
# <span data-ttu-id="4222b-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4222b-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="4222b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4222b-102">SYNOPSIS</span></span>
<span data-ttu-id="4222b-103">Modyfikuje element webhook dla elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4222b-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="4222b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4222b-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4222b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4222b-105">DESCRIPTION</span></span>
<span data-ttu-id="4222b-106">Polecenie cmdlet **Set-AzAutomationWebhook** modyfikuje element webhook dla elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4222b-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="4222b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4222b-107">EXAMPLES</span></span>

### <span data-ttu-id="4222b-108">Przykład 1. wyłączenie elementu webhook</span><span class="sxs-lookup"><span data-stu-id="4222b-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="4222b-109">To polecenie wyłącza element webhook o nazwie Webhook01 na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="4222b-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="4222b-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4222b-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="4222b-111">To polecenie ustawia wartość Uruchom na dla elementu webhook i wymusza uruchomienie elementu Runbook w grupie hybrydowej procesu roboczego o nazwie Windows.</span><span class="sxs-lookup"><span data-stu-id="4222b-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="4222b-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4222b-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="4222b-113">To polecenie aktualizuje wartość Uruchom dla elementu webhook i wymusza uruchomienie elementu Runbook w ramach procesu roboczego usługi Azure Runbook.</span><span class="sxs-lookup"><span data-stu-id="4222b-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="4222b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4222b-114">PARAMETERS</span></span>

### <span data-ttu-id="4222b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4222b-115">-AutomationAccountName</span></span>
<span data-ttu-id="4222b-116">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet modyfikuje element webhook.</span><span class="sxs-lookup"><span data-stu-id="4222b-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="4222b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4222b-117">-DefaultProfile</span></span>
<span data-ttu-id="4222b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4222b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4222b-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="4222b-119">-IsEnabled</span></span>
<span data-ttu-id="4222b-120">Określa, czy element webhook jest włączony.</span><span class="sxs-lookup"><span data-stu-id="4222b-120">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4222b-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4222b-121">-Name</span></span>
<span data-ttu-id="4222b-122">Określa nazwę elementu webhook, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4222b-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4222b-123">— Parametry</span><span class="sxs-lookup"><span data-stu-id="4222b-123">-Parameters</span></span>
<span data-ttu-id="4222b-124">Określa słownik par kluczy/wartości.</span><span class="sxs-lookup"><span data-stu-id="4222b-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="4222b-125">Klucze są nazwami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="4222b-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="4222b-126">Wartości są wartościami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="4222b-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="4222b-127">Po uruchomieniu elementu Runbook w odpowiedzi na element webhook te parametry są przekazywane do elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="4222b-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4222b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4222b-128">-ResourceGroupName</span></span>
<span data-ttu-id="4222b-129">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje element webhook.</span><span class="sxs-lookup"><span data-stu-id="4222b-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="4222b-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="4222b-130">-RunOn</span></span>
<span data-ttu-id="4222b-131">Opcjonalna nazwa agenta hybrydowego, który powinien wykonywać element Runbook</span><span class="sxs-lookup"><span data-stu-id="4222b-131">Optional name of the hybrid agent which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4222b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4222b-132">CommonParameters</span></span>
<span data-ttu-id="4222b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4222b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4222b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4222b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4222b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4222b-135">INPUTS</span></span>

### <span data-ttu-id="4222b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4222b-136">System.String</span></span>

### <span data-ttu-id="4222b-137">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4222b-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4222b-138">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="4222b-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="4222b-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4222b-139">OUTPUTS</span></span>

### <span data-ttu-id="4222b-140">Microsoft. Azure. Commands. Automation. model. webhook</span><span class="sxs-lookup"><span data-stu-id="4222b-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="4222b-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4222b-141">NOTES</span></span>

## <span data-ttu-id="4222b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4222b-142">RELATED LINKS</span></span>

[<span data-ttu-id="4222b-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4222b-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="4222b-144">Nowe — AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4222b-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="4222b-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4222b-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)



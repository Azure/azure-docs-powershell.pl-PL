---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 200cc0b6312940606bb4e75f576c60928a84b33f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009802"
---
# <span data-ttu-id="9bd55-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9bd55-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="9bd55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd55-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd55-103">Modyfikuje webhook dla podręcznika automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9bd55-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="9bd55-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9bd55-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bd55-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9bd55-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd55-106">Polecenie **cmdlet Set-AzAutomationWebhook** modyfikuje webhook dla podręcznika Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9bd55-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="9bd55-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9bd55-107">EXAMPLES</span></span>

### <span data-ttu-id="9bd55-108">Przykład 1. Wyłączanie aplikacji WebHook</span><span class="sxs-lookup"><span data-stu-id="9bd55-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="9bd55-109">To polecenie wyłącza webhook o nazwie Webhook01 na koncie automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="9bd55-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="9bd55-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9bd55-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="9bd55-111">To polecenie ustawia wartość uruchamiania dla sieci Webhook i wymusza uruchomienie podręcznika w grupie Pracownik hybrydowy o nazwie Windows.</span><span class="sxs-lookup"><span data-stu-id="9bd55-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="9bd55-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9bd55-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="9bd55-113">To polecenie aktualizuje wartość uruchomienia dla sieci Webhook i wymusza uruchomienie podręcznika na pracowniku azure runbook.</span><span class="sxs-lookup"><span data-stu-id="9bd55-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="9bd55-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bd55-114">PARAMETERS</span></span>

### <span data-ttu-id="9bd55-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9bd55-115">-AutomationAccountName</span></span>
<span data-ttu-id="9bd55-116">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet modyfikuje webhook.</span><span class="sxs-lookup"><span data-stu-id="9bd55-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="9bd55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd55-117">-DefaultProfile</span></span>
<span data-ttu-id="9bd55-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9bd55-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bd55-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="9bd55-119">-IsEnabled</span></span>
<span data-ttu-id="9bd55-120">Określa, czy sieć Webhook jest włączona.</span><span class="sxs-lookup"><span data-stu-id="9bd55-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="9bd55-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9bd55-121">-Name</span></span>
<span data-ttu-id="9bd55-122">Określa nazwę sieci Web, dla których to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="9bd55-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9bd55-123">— Parametry</span><span class="sxs-lookup"><span data-stu-id="9bd55-123">-Parameters</span></span>
<span data-ttu-id="9bd55-124">Określa słownik par klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="9bd55-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="9bd55-125">Klucze to nazwy parametrów podręcznika obsługi.</span><span class="sxs-lookup"><span data-stu-id="9bd55-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="9bd55-126">Wartości są wartościami parametrów podręcznika uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="9bd55-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="9bd55-127">Po uruchomieniu podręcznika w odpowiedzi na witrynę internetową te parametry są przekazywane do tego podręcznika.</span><span class="sxs-lookup"><span data-stu-id="9bd55-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="9bd55-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd55-128">-ResourceGroupName</span></span>
<span data-ttu-id="9bd55-129">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje webhook.</span><span class="sxs-lookup"><span data-stu-id="9bd55-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="9bd55-130">- RunOn</span><span class="sxs-lookup"><span data-stu-id="9bd55-130">-RunOn</span></span>
<span data-ttu-id="9bd55-131">Opcjonalna nazwa agenta hybrydowego, który powinien wykonać podręcznik</span><span class="sxs-lookup"><span data-stu-id="9bd55-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="9bd55-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd55-132">CommonParameters</span></span>
<span data-ttu-id="9bd55-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd55-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd55-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bd55-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd55-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bd55-135">INPUTS</span></span>

### <span data-ttu-id="9bd55-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9bd55-136">System.String</span></span>

### <span data-ttu-id="9bd55-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9bd55-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9bd55-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="9bd55-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="9bd55-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bd55-139">OUTPUTS</span></span>

### <span data-ttu-id="9bd55-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="9bd55-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="9bd55-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9bd55-141">NOTES</span></span>

## <span data-ttu-id="9bd55-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bd55-142">RELATED LINKS</span></span>

[<span data-ttu-id="9bd55-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9bd55-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="9bd55-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9bd55-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="9bd55-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9bd55-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)



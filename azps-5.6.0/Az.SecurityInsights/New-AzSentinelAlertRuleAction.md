---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: ed4d1b5d833ce73a9b0a19e38a05192d11a0d8f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976362"
---
# <span data-ttu-id="122ce-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="122ce-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="122ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="122ce-102">SYNOPSIS</span></span>
<span data-ttu-id="122ce-103">Dodawanie automatycznej odpowiedzi do analiz analitycznych.</span><span class="sxs-lookup"><span data-stu-id="122ce-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="122ce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="122ce-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="122ce-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="122ce-105">DESCRIPTION</span></span>
<span data-ttu-id="122ce-106">Polecenie **cmdlet New-AzSentinelAlertRuleAction** tworzy automatyczną odpowiedź dla reguły alertu w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="122ce-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="122ce-107">Musisz podać identyfikator ponownego logiki aplikacji i identyfikator Uri wyzwalacza, które można znaleźć przy użyciu modułu aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="122ce-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="122ce-108">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="122ce-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="122ce-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="122ce-109">EXAMPLES</span></span>

### <span data-ttu-id="122ce-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="122ce-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="122ce-111">W tym przykładzie jest obiektu **alertRuleAction** dla określonej reguły alertu przy użyciu właściwości aplikacji logiki, a następnie jest on przechowywał w $AlertRuleAction alertu.</span><span class="sxs-lookup"><span data-stu-id="122ce-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="122ce-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="122ce-112">PARAMETERS</span></span>

### <span data-ttu-id="122ce-113">- ActionId</span><span class="sxs-lookup"><span data-stu-id="122ce-113">-ActionId</span></span>
<span data-ttu-id="122ce-114">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="122ce-114">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122ce-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="122ce-115">-AlertRuleId</span></span>
<span data-ttu-id="122ce-116">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="122ce-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122ce-117">-DefaultProfile</span></span>
<span data-ttu-id="122ce-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="122ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="122ce-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="122ce-119">-LogicAppResourceId</span></span>
<span data-ttu-id="122ce-120">Identyfikator zasobu aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="122ce-120">Action Logic App Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="122ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="122ce-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="122ce-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122ce-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="122ce-123">-TriggerUri</span></span>
<span data-ttu-id="122ce-124">Uri wyzwalacza aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="122ce-124">Action Logic App Trigger Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122ce-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="122ce-125">-WorkspaceName</span></span>
<span data-ttu-id="122ce-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="122ce-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122ce-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="122ce-127">-Confirm</span></span>
<span data-ttu-id="122ce-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="122ce-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122ce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="122ce-129">-WhatIf</span></span>
<span data-ttu-id="122ce-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="122ce-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="122ce-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="122ce-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122ce-132">CommonParameters</span></span>
<span data-ttu-id="122ce-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122ce-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="122ce-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122ce-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="122ce-135">INPUTS</span></span>

### <span data-ttu-id="122ce-136">Brak</span><span class="sxs-lookup"><span data-stu-id="122ce-136">None</span></span>
## <span data-ttu-id="122ce-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="122ce-137">OUTPUTS</span></span>

### <span data-ttu-id="122ce-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="122ce-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="122ce-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="122ce-139">NOTES</span></span>

## <span data-ttu-id="122ce-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="122ce-140">RELATED LINKS</span></span>

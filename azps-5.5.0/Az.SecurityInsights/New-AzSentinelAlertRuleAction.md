---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201746"
---
# <span data-ttu-id="9de7d-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="9de7d-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="9de7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de7d-102">SYNOPSIS</span></span>
<span data-ttu-id="9de7d-103">Dodawanie automatycznej odpowiedzi do analiz analitycznych.</span><span class="sxs-lookup"><span data-stu-id="9de7d-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="9de7d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9de7d-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9de7d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9de7d-105">DESCRIPTION</span></span>
<span data-ttu-id="9de7d-106">Polecenie **cmdlet New-AzSentinelAlertRuleAction** tworzy automatyczną odpowiedź dla reguły alertu w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9de7d-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="9de7d-107">Musisz podać identyfikator ponownego logiki aplikacji i identyfikator Uri wyzwalacza, które można znaleźć przy użyciu modułu aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="9de7d-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="9de7d-108">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9de7d-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9de7d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9de7d-109">EXAMPLES</span></span>

### <span data-ttu-id="9de7d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9de7d-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="9de7d-111">W tym przykładzie **jest określonej** reguły alertu, która jest określana przy użyciu właściwości aplikacji logiki, a następnie jest ona przechowywała w $AlertRuleAction alertu.</span><span class="sxs-lookup"><span data-stu-id="9de7d-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="9de7d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9de7d-112">PARAMETERS</span></span>

### <span data-ttu-id="9de7d-113">- ActionId</span><span class="sxs-lookup"><span data-stu-id="9de7d-113">-ActionId</span></span>
<span data-ttu-id="9de7d-114">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="9de7d-114">Action Id.</span></span>

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

### <span data-ttu-id="9de7d-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="9de7d-115">-AlertRuleId</span></span>
<span data-ttu-id="9de7d-116">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="9de7d-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="9de7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de7d-117">-DefaultProfile</span></span>
<span data-ttu-id="9de7d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9de7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de7d-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="9de7d-119">-LogicAppResourceId</span></span>
<span data-ttu-id="9de7d-120">Identyfikator zasobu aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="9de7d-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="9de7d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de7d-121">-ResourceGroupName</span></span>
<span data-ttu-id="9de7d-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9de7d-122">Resource group name.</span></span>

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

### <span data-ttu-id="9de7d-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="9de7d-123">-TriggerUri</span></span>
<span data-ttu-id="9de7d-124">Uri wyzwalacza aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="9de7d-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="9de7d-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9de7d-125">-WorkspaceName</span></span>
<span data-ttu-id="9de7d-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9de7d-126">Workspace Name.</span></span>

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

### <span data-ttu-id="9de7d-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9de7d-127">-Confirm</span></span>
<span data-ttu-id="9de7d-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9de7d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de7d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de7d-129">-WhatIf</span></span>
<span data-ttu-id="9de7d-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9de7d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9de7d-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9de7d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de7d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de7d-132">CommonParameters</span></span>
<span data-ttu-id="9de7d-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de7d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de7d-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9de7d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de7d-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de7d-135">INPUTS</span></span>

### <span data-ttu-id="9de7d-136">Brak</span><span class="sxs-lookup"><span data-stu-id="9de7d-136">None</span></span>
## <span data-ttu-id="9de7d-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9de7d-137">OUTPUTS</span></span>

### <span data-ttu-id="9de7d-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="9de7d-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="9de7d-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9de7d-139">NOTES</span></span>

## <span data-ttu-id="9de7d-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9de7d-140">RELATED LINKS</span></span>

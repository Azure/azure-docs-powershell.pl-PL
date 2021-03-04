---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 3feb6a9cfa06e06a4759c34e3c0b2cd624559d2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955649"
---
# <span data-ttu-id="601de-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="601de-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="601de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="601de-102">SYNOPSIS</span></span>
<span data-ttu-id="601de-103">Aktualizowanie automatycznej odpowiedzi (akcji reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="601de-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="601de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="601de-104">SYNTAX</span></span>

### <span data-ttu-id="601de-105">ActionId (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="601de-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601de-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="601de-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="601de-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="601de-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="601de-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="601de-108">DESCRIPTION</span></span>
<span data-ttu-id="601de-109">Polecenie **cmdlet Update-AzSentinelAlertRuleAction** aktualizuje zakładkę w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="601de-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="601de-110">Obiekt **AlertRuleAction** można przekazać jako parametr lub za pomocą operatora potoku albo określić parametry *AlertRuleId* i *ActionId.*</span><span class="sxs-lookup"><span data-stu-id="601de-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="601de-111">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="601de-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="601de-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="601de-112">EXAMPLES</span></span>

### <span data-ttu-id="601de-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="601de-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="601de-114">W tym przykładzie **jest aktualizowana akcja AlertRuleAction** zastępująca istniejącą *akcję* nowymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="601de-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="601de-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="601de-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="601de-116">W tym przykładzie **jest aktualizowana akcja AlertRuleAction,** zastępując istniejącą akcję nowymi właściwościami przy użyciu obiektu InputObject. </span><span class="sxs-lookup"><span data-stu-id="601de-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="601de-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="601de-117">PARAMETERS</span></span>

### <span data-ttu-id="601de-118">- ActionId</span><span class="sxs-lookup"><span data-stu-id="601de-118">-ActionId</span></span>
<span data-ttu-id="601de-119">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="601de-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601de-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="601de-120">-AlertRuleId</span></span>
<span data-ttu-id="601de-121">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="601de-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601de-122">-DefaultProfile</span></span>
<span data-ttu-id="601de-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="601de-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="601de-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="601de-124">-InputObject</span></span>
<span data-ttu-id="601de-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="601de-125">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="601de-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="601de-126">-LogicAppResourceId</span></span>
<span data-ttu-id="601de-127">Identyfikator zasobu aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="601de-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="601de-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="601de-128">-ResourceGroupName</span></span>
<span data-ttu-id="601de-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="601de-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601de-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="601de-130">-ResourceId</span></span>
<span data-ttu-id="601de-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="601de-131">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="601de-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="601de-132">-TriggerUri</span></span>
<span data-ttu-id="601de-133">Uri wyzwalacza aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="601de-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="601de-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="601de-134">-WorkspaceName</span></span>
<span data-ttu-id="601de-135">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="601de-135">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601de-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="601de-136">-Confirm</span></span>
<span data-ttu-id="601de-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="601de-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="601de-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="601de-138">-WhatIf</span></span>
<span data-ttu-id="601de-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="601de-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="601de-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="601de-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="601de-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601de-141">CommonParameters</span></span>
<span data-ttu-id="601de-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="601de-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601de-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="601de-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601de-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="601de-144">INPUTS</span></span>

### <span data-ttu-id="601de-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="601de-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="601de-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="601de-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="601de-147">System.String</span><span class="sxs-lookup"><span data-stu-id="601de-147">System.String</span></span>

## <span data-ttu-id="601de-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="601de-148">OUTPUTS</span></span>

### <span data-ttu-id="601de-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="601de-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="601de-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="601de-150">NOTES</span></span>

## <span data-ttu-id="601de-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="601de-151">RELATED LINKS</span></span>

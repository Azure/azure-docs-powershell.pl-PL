---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 03eb85c423b06642a15db616b1ba1e0343c94963
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502952"
---
# <span data-ttu-id="76406-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="76406-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="76406-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76406-102">SYNOPSIS</span></span>
<span data-ttu-id="76406-103">Aktualizowanie odpowiedzi automatycznej (akcji reguły alertu).</span><span class="sxs-lookup"><span data-stu-id="76406-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="76406-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76406-104">SYNTAX</span></span>

### <span data-ttu-id="76406-105">ActionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="76406-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76406-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="76406-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76406-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="76406-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76406-108">Opis</span><span class="sxs-lookup"><span data-stu-id="76406-108">DESCRIPTION</span></span>
<span data-ttu-id="76406-109">Polecenie cmdlet **Update-AzSentinelAlertRuleAction** umożliwia zaktualizowanie zakładki w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="76406-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="76406-110">Obiekt **AlertRuleAction** można przekazać jako parametr lub za pomocą operatora potoku albo też określić parametry *AlertRuleId* i *ActionID* .</span><span class="sxs-lookup"><span data-stu-id="76406-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="76406-111">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76406-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="76406-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76406-112">EXAMPLES</span></span>

### <span data-ttu-id="76406-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76406-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="76406-114">W tym przykładzie Zaktualizowano **AlertRuleAction** zastąpienie istniejącej *akcji* nowymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="76406-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="76406-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="76406-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="76406-116">W tym przykładzie Zaktualizowano **AlertRuleAction** przy użyciu funkcji inputobject zastępując istniejącą *akcję* nowymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="76406-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="76406-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76406-117">PARAMETERS</span></span>

### <span data-ttu-id="76406-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="76406-118">-ActionId</span></span>
<span data-ttu-id="76406-119">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="76406-119">Action Id.</span></span>

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

### <span data-ttu-id="76406-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="76406-120">-AlertRuleId</span></span>
<span data-ttu-id="76406-121">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="76406-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="76406-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76406-122">-DefaultProfile</span></span>
<span data-ttu-id="76406-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76406-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76406-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76406-124">-InputObject</span></span>
<span data-ttu-id="76406-125">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="76406-125">InputObject.</span></span>

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

### <span data-ttu-id="76406-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="76406-126">-LogicAppResourceId</span></span>
<span data-ttu-id="76406-127">Identyfikator zasobu aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="76406-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="76406-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76406-128">-ResourceGroupName</span></span>
<span data-ttu-id="76406-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76406-129">Resource group name.</span></span>

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

### <span data-ttu-id="76406-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76406-130">-ResourceId</span></span>
<span data-ttu-id="76406-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="76406-131">Resource Id.</span></span>

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

### <span data-ttu-id="76406-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="76406-132">-TriggerUri</span></span>
<span data-ttu-id="76406-133">Identyfikator URI wyzwalacza aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="76406-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="76406-134">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="76406-134">-WorkspaceName</span></span>
<span data-ttu-id="76406-135">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="76406-135">Workspace Name.</span></span>

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

### <span data-ttu-id="76406-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76406-136">-Confirm</span></span>
<span data-ttu-id="76406-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76406-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76406-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76406-138">-WhatIf</span></span>
<span data-ttu-id="76406-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76406-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76406-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76406-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76406-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76406-141">CommonParameters</span></span>
<span data-ttu-id="76406-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76406-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76406-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76406-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76406-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76406-144">INPUTS</span></span>

### <span data-ttu-id="76406-145">Microsoft. Azure. Commands. SecurityInsights. models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="76406-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="76406-146">Microsoft. Azure. Commands. SecurityInsights. models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="76406-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="76406-147">System. String</span><span class="sxs-lookup"><span data-stu-id="76406-147">System.String</span></span>

## <span data-ttu-id="76406-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76406-148">OUTPUTS</span></span>

### <span data-ttu-id="76406-149">Microsoft. Azure. Commands. SecurityInsights. models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="76406-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="76406-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76406-150">NOTES</span></span>

## <span data-ttu-id="76406-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76406-151">RELATED LINKS</span></span>

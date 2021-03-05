---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 0828961a534a6f98d52cdf8c4e2a134cc2975df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963633"
---
# <span data-ttu-id="84697-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="84697-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="84697-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84697-102">SYNOPSIS</span></span>
<span data-ttu-id="84697-103">Usuwanie automatycznej odpowiedzi z analiz analitycznych.</span><span class="sxs-lookup"><span data-stu-id="84697-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="84697-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84697-104">SYNTAX</span></span>

### <span data-ttu-id="84697-105">ActionId (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="84697-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84697-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="84697-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84697-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="84697-107">DESCRIPTION</span></span>
<span data-ttu-id="84697-108">Polecenie cmdlet **Remove-AzSentinelAlertRuleAction** trwale usuwa automatyczną odpowiedź z reguły alertu w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="84697-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="84697-109">Obiekt **AlertRuleAction** można przekazać za pomocą operatora potoku lub ewentualnie określić wymagane parametry.</span><span class="sxs-lookup"><span data-stu-id="84697-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="84697-110">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84697-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="84697-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84697-111">EXAMPLES</span></span>

### <span data-ttu-id="84697-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84697-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="84697-113">To polecenie usuwa regułę alertu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="84697-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="84697-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84697-114">PARAMETERS</span></span>

### <span data-ttu-id="84697-115">- ActionId</span><span class="sxs-lookup"><span data-stu-id="84697-115">-ActionId</span></span>
<span data-ttu-id="84697-116">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="84697-116">Action Id.</span></span>

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

### <span data-ttu-id="84697-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="84697-117">-AlertRuleId</span></span>
<span data-ttu-id="84697-118">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="84697-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84697-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84697-119">-DefaultProfile</span></span>
<span data-ttu-id="84697-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="84697-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84697-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84697-121">-InputObject</span></span>
<span data-ttu-id="84697-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="84697-122">InputObject.</span></span>

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

### <span data-ttu-id="84697-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84697-123">-PassThru</span></span>
<span data-ttu-id="84697-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="84697-124">PassThru</span></span>

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

### <span data-ttu-id="84697-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84697-125">-ResourceGroupName</span></span>
<span data-ttu-id="84697-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84697-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84697-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84697-127">-WorkspaceName</span></span>
<span data-ttu-id="84697-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="84697-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84697-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84697-129">-Confirm</span></span>
<span data-ttu-id="84697-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84697-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84697-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84697-131">-WhatIf</span></span>
<span data-ttu-id="84697-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84697-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84697-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="84697-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84697-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84697-134">CommonParameters</span></span>
<span data-ttu-id="84697-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84697-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84697-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84697-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84697-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84697-137">INPUTS</span></span>

### <span data-ttu-id="84697-138">System.String</span><span class="sxs-lookup"><span data-stu-id="84697-138">System.String</span></span>
### <span data-ttu-id="84697-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="84697-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="84697-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84697-140">OUTPUTS</span></span>

### <span data-ttu-id="84697-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="84697-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="84697-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84697-142">NOTES</span></span>

## <span data-ttu-id="84697-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84697-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: af63ecd604f6ea7e475fcc8034a4e4b6d532069e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963649"
---
# <span data-ttu-id="26195-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="26195-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="26195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26195-102">SYNOPSIS</span></span>
<span data-ttu-id="26195-103">Usuwanie danych analitycznych.</span><span class="sxs-lookup"><span data-stu-id="26195-103">Delete an Analytic.</span></span>

## <span data-ttu-id="26195-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26195-104">SYNTAX</span></span>

### <span data-ttu-id="26195-105">AlertRuleId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="26195-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26195-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="26195-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26195-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="26195-107">DESCRIPTION</span></span>
<span data-ttu-id="26195-108">Polecenie **cmdlet Remove-AzSentinelAlertRule** trwale usuwa regułę alertu z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="26195-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="26195-109">Obiekt **AlertRule można** przekazać za pomocą operatora potoku lub ewentualnie określić wymagane parametry.</span><span class="sxs-lookup"><span data-stu-id="26195-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="26195-110">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26195-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="26195-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26195-111">EXAMPLES</span></span>

### <span data-ttu-id="26195-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26195-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="26195-113">To polecenie usuwa regułę alertu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="26195-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="26195-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26195-114">PARAMETERS</span></span>

### <span data-ttu-id="26195-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="26195-115">-AlertRuleId</span></span>
<span data-ttu-id="26195-116">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="26195-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26195-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26195-117">-DefaultProfile</span></span>
<span data-ttu-id="26195-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="26195-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26195-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26195-119">-InputObject</span></span>
<span data-ttu-id="26195-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="26195-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26195-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26195-121">-PassThru</span></span>
<span data-ttu-id="26195-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="26195-122">PassThru</span></span>

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

### <span data-ttu-id="26195-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26195-123">-ResourceGroupName</span></span>
<span data-ttu-id="26195-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26195-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26195-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="26195-125">-WorkspaceName</span></span>
<span data-ttu-id="26195-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="26195-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26195-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26195-127">-Confirm</span></span>
<span data-ttu-id="26195-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26195-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26195-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26195-129">-WhatIf</span></span>
<span data-ttu-id="26195-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26195-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26195-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="26195-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26195-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26195-132">CommonParameters</span></span>
<span data-ttu-id="26195-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26195-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26195-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26195-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26195-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26195-135">INPUTS</span></span>

### <span data-ttu-id="26195-136">System.String</span><span class="sxs-lookup"><span data-stu-id="26195-136">System.String</span></span>
### <span data-ttu-id="26195-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="26195-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="26195-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26195-138">OUTPUTS</span></span>

### <span data-ttu-id="26195-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="26195-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="26195-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26195-140">NOTES</span></span>

## <span data-ttu-id="26195-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26195-141">RELATED LINKS</span></span>

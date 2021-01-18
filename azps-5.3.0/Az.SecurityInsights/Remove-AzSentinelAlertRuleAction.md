---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502961"
---
# <span data-ttu-id="60aee-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="60aee-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="60aee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60aee-102">SYNOPSIS</span></span>
<span data-ttu-id="60aee-103">Usuwanie automatycznej odpowiedzi z raportu analitycznego.</span><span class="sxs-lookup"><span data-stu-id="60aee-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="60aee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60aee-104">SYNTAX</span></span>

### <span data-ttu-id="60aee-105">ActionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60aee-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60aee-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="60aee-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60aee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="60aee-107">DESCRIPTION</span></span>
<span data-ttu-id="60aee-108">Polecenie cmdlet **Remove-AzSentinelAlertRuleAction** trwale usuwa odpowiedź automatyczną z reguły alertu w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="60aee-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="60aee-109">Obiekt **AlertRuleAction** można przekazać za pomocą operatora potoku lub można też określić parametry wymagane.</span><span class="sxs-lookup"><span data-stu-id="60aee-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="60aee-110">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="60aee-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="60aee-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60aee-111">EXAMPLES</span></span>

### <span data-ttu-id="60aee-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60aee-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="60aee-113">To polecenie usuwa regułę alertu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="60aee-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="60aee-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60aee-114">PARAMETERS</span></span>

### <span data-ttu-id="60aee-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="60aee-115">-ActionId</span></span>
<span data-ttu-id="60aee-116">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="60aee-116">Action Id.</span></span>

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

### <span data-ttu-id="60aee-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="60aee-117">-AlertRuleId</span></span>
<span data-ttu-id="60aee-118">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="60aee-118">Alert Rule Id.</span></span>

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

### <span data-ttu-id="60aee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60aee-119">-DefaultProfile</span></span>
<span data-ttu-id="60aee-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60aee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60aee-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="60aee-121">-InputObject</span></span>
<span data-ttu-id="60aee-122">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="60aee-122">InputObject.</span></span>

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

### <span data-ttu-id="60aee-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60aee-123">-PassThru</span></span>
<span data-ttu-id="60aee-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="60aee-124">PassThru</span></span>

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

### <span data-ttu-id="60aee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60aee-125">-ResourceGroupName</span></span>
<span data-ttu-id="60aee-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="60aee-126">Resource group name.</span></span>

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

### <span data-ttu-id="60aee-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="60aee-127">-WorkspaceName</span></span>
<span data-ttu-id="60aee-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="60aee-128">Workspace Name.</span></span>

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

### <span data-ttu-id="60aee-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60aee-129">-Confirm</span></span>
<span data-ttu-id="60aee-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60aee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60aee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60aee-131">-WhatIf</span></span>
<span data-ttu-id="60aee-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60aee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60aee-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60aee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60aee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60aee-134">CommonParameters</span></span>
<span data-ttu-id="60aee-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60aee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60aee-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60aee-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60aee-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60aee-137">INPUTS</span></span>

### <span data-ttu-id="60aee-138">System. String</span><span class="sxs-lookup"><span data-stu-id="60aee-138">System.String</span></span>
### <span data-ttu-id="60aee-139">Microsoft. Azure. Commands. SecurityInsights. models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="60aee-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="60aee-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60aee-140">OUTPUTS</span></span>

### <span data-ttu-id="60aee-141">Microsoft. Azure. Commands. SecurityInsights. models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="60aee-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="60aee-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60aee-142">NOTES</span></span>

## <span data-ttu-id="60aee-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60aee-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502963"
---
# <span data-ttu-id="387da-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="387da-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="387da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="387da-102">SYNOPSIS</span></span>
<span data-ttu-id="387da-103">Usuwanie raportu analitycznego.</span><span class="sxs-lookup"><span data-stu-id="387da-103">Delete an Analytic.</span></span>

## <span data-ttu-id="387da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="387da-104">SYNTAX</span></span>

### <span data-ttu-id="387da-105">AlertRuleId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="387da-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="387da-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="387da-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="387da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="387da-107">DESCRIPTION</span></span>
<span data-ttu-id="387da-108">Polecenie cmdlet **Remove-AzSentinelAlertRule** powoduje trwałe usunięcie reguły alertu z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="387da-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="387da-109">Obiekt **AlertRule** można przekazać za pomocą operatora potoku lub można też określić parametry wymagane.</span><span class="sxs-lookup"><span data-stu-id="387da-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="387da-110">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="387da-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="387da-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="387da-111">EXAMPLES</span></span>

### <span data-ttu-id="387da-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="387da-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="387da-113">To polecenie usuwa regułę alertu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="387da-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="387da-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="387da-114">PARAMETERS</span></span>

### <span data-ttu-id="387da-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="387da-115">-AlertRuleId</span></span>
<span data-ttu-id="387da-116">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="387da-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="387da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387da-117">-DefaultProfile</span></span>
<span data-ttu-id="387da-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="387da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="387da-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="387da-119">-InputObject</span></span>
<span data-ttu-id="387da-120">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="387da-120">InputObject.</span></span>

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

### <span data-ttu-id="387da-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="387da-121">-PassThru</span></span>
<span data-ttu-id="387da-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="387da-122">PassThru</span></span>

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

### <span data-ttu-id="387da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387da-123">-ResourceGroupName</span></span>
<span data-ttu-id="387da-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="387da-124">Resource group name.</span></span>

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

### <span data-ttu-id="387da-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="387da-125">-WorkspaceName</span></span>
<span data-ttu-id="387da-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="387da-126">Workspace Name.</span></span>

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

### <span data-ttu-id="387da-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="387da-127">-Confirm</span></span>
<span data-ttu-id="387da-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="387da-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="387da-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="387da-129">-WhatIf</span></span>
<span data-ttu-id="387da-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="387da-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="387da-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="387da-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="387da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387da-132">CommonParameters</span></span>
<span data-ttu-id="387da-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="387da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387da-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="387da-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387da-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="387da-135">INPUTS</span></span>

### <span data-ttu-id="387da-136">System. String</span><span class="sxs-lookup"><span data-stu-id="387da-136">System.String</span></span>
### <span data-ttu-id="387da-137">Microsoft. Azure. Commands. SecurityInsights. models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="387da-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="387da-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="387da-138">OUTPUTS</span></span>

### <span data-ttu-id="387da-139">Microsoft. Azure. Commands. SecurityInsights. models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="387da-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="387da-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="387da-140">NOTES</span></span>

## <span data-ttu-id="387da-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="387da-141">RELATED LINKS</span></span>

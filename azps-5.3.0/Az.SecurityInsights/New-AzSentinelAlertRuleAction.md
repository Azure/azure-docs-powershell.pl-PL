---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502977"
---
# <span data-ttu-id="a786a-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="a786a-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="a786a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a786a-102">SYNOPSIS</span></span>
<span data-ttu-id="a786a-103">Dodanie automatycznej odpowiedzi do Analatic.</span><span class="sxs-lookup"><span data-stu-id="a786a-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="a786a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a786a-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a786a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a786a-105">DESCRIPTION</span></span>
<span data-ttu-id="a786a-106">Polecenie cmdlet **New-AzSentinelAlertRuleAction** tworzy automatyczną odpowiedź dla reguły alertu w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a786a-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="a786a-107">Musisz dostarczyć identyfikator URI aplikacji resorce, który można znaleźć przy użyciu modułu aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="a786a-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="a786a-108">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a786a-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a786a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a786a-109">EXAMPLES</span></span>

### <span data-ttu-id="a786a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a786a-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="a786a-111">W tym przykładzie przedstawiono tworzenie **AlertRuleAction** dla określonej reguły alertu przy użyciu właściwości aplikacji logicznej, a następnie zapisanie jej w zmiennej $AlertRuleAction.</span><span class="sxs-lookup"><span data-stu-id="a786a-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="a786a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a786a-112">PARAMETERS</span></span>

### <span data-ttu-id="a786a-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="a786a-113">-ActionId</span></span>
<span data-ttu-id="a786a-114">Identyfikator akcji.</span><span class="sxs-lookup"><span data-stu-id="a786a-114">Action Id.</span></span>

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

### <span data-ttu-id="a786a-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a786a-115">-AlertRuleId</span></span>
<span data-ttu-id="a786a-116">Identyfikator reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="a786a-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="a786a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a786a-117">-DefaultProfile</span></span>
<span data-ttu-id="a786a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a786a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a786a-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="a786a-119">-LogicAppResourceId</span></span>
<span data-ttu-id="a786a-120">Identyfikator zasobu aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="a786a-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="a786a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a786a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a786a-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a786a-122">Resource group name.</span></span>

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

### <span data-ttu-id="a786a-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="a786a-123">-TriggerUri</span></span>
<span data-ttu-id="a786a-124">Identyfikator URI wyzwalacza aplikacji logiki akcji.</span><span class="sxs-lookup"><span data-stu-id="a786a-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="a786a-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a786a-125">-WorkspaceName</span></span>
<span data-ttu-id="a786a-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a786a-126">Workspace Name.</span></span>

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

### <span data-ttu-id="a786a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a786a-127">-Confirm</span></span>
<span data-ttu-id="a786a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a786a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a786a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a786a-129">-WhatIf</span></span>
<span data-ttu-id="a786a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a786a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a786a-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a786a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a786a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a786a-132">CommonParameters</span></span>
<span data-ttu-id="a786a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a786a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a786a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a786a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a786a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a786a-135">INPUTS</span></span>

### <span data-ttu-id="a786a-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a786a-136">None</span></span>
## <span data-ttu-id="a786a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a786a-137">OUTPUTS</span></span>

### <span data-ttu-id="a786a-138">Microsoft. Azure. Commands. SecurityInsights. models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="a786a-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="a786a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a786a-139">NOTES</span></span>

## <span data-ttu-id="a786a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a786a-140">RELATED LINKS</span></span>

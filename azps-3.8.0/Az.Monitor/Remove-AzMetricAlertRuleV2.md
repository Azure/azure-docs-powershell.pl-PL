---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894261"
---
# <span data-ttu-id="826fd-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="826fd-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="826fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="826fd-102">SYNOPSIS</span></span>
<span data-ttu-id="826fd-103">Usuwa regułę alertu metryki v2 (nie klasyczna).</span><span class="sxs-lookup"><span data-stu-id="826fd-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="826fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="826fd-104">SYNTAX</span></span>

### <span data-ttu-id="826fd-105">ByMetricRuleResourceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="826fd-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="826fd-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="826fd-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="826fd-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="826fd-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="826fd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="826fd-108">DESCRIPTION</span></span>
<span data-ttu-id="826fd-109">Polecenie cmdlet **Remove-AzMetricAlertRuleV2** umożliwia usunięcie reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="826fd-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="826fd-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="826fd-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="826fd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="826fd-111">EXAMPLES</span></span>

### <span data-ttu-id="826fd-112">Przykład 1: Usuwanie reguły alertu według nazwy</span><span class="sxs-lookup"><span data-stu-id="826fd-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="826fd-113">To polecenie usuwa regułę alertu o nazwie PsSdk</span><span class="sxs-lookup"><span data-stu-id="826fd-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="826fd-114">Przykład 2: Usuwanie reguły alertu według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="826fd-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="826fd-115">To polecenie usuwa regułę alertu z IDENTYFIKATORem zasobu `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="826fd-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="826fd-116">Przykład 3: otrzymywanie alertu i usuwanie go</span><span class="sxs-lookup"><span data-stu-id="826fd-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="826fd-117">To polecenie pobiera alert i usuwa go.</span><span class="sxs-lookup"><span data-stu-id="826fd-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="826fd-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="826fd-118">PARAMETERS</span></span>

### <span data-ttu-id="826fd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="826fd-119">-AsJob</span></span>
<span data-ttu-id="826fd-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="826fd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="826fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="826fd-121">-DefaultProfile</span></span>
<span data-ttu-id="826fd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="826fd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="826fd-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="826fd-123">-InputObject</span></span>
<span data-ttu-id="826fd-124">Obiekt reguły metryki</span><span class="sxs-lookup"><span data-stu-id="826fd-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="826fd-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="826fd-125">-Name</span></span>
<span data-ttu-id="826fd-126">Nazwa reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="826fd-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="826fd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="826fd-127">-PassThru</span></span>
<span data-ttu-id="826fd-128">Zwraca wartość Prawda po udanym usunięciu.</span><span class="sxs-lookup"><span data-stu-id="826fd-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="826fd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="826fd-129">-ResourceGroupName</span></span>
<span data-ttu-id="826fd-130">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="826fd-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="826fd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="826fd-131">-ResourceId</span></span>
<span data-ttu-id="826fd-132">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="826fd-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="826fd-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="826fd-133">-Confirm</span></span>
<span data-ttu-id="826fd-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="826fd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="826fd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="826fd-135">-WhatIf</span></span>
<span data-ttu-id="826fd-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="826fd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="826fd-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="826fd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="826fd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="826fd-138">CommonParameters</span></span>
<span data-ttu-id="826fd-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="826fd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="826fd-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="826fd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="826fd-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="826fd-141">INPUTS</span></span>

### <span data-ttu-id="826fd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="826fd-142">System.String</span></span>

### <span data-ttu-id="826fd-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="826fd-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="826fd-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="826fd-144">OUTPUTS</span></span>

### <span data-ttu-id="826fd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="826fd-145">System.Boolean</span></span>

## <span data-ttu-id="826fd-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="826fd-146">NOTES</span></span>

## <span data-ttu-id="826fd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="826fd-147">RELATED LINKS</span></span>

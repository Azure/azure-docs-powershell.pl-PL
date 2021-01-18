---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499681"
---
# <span data-ttu-id="f8463-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f8463-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="f8463-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8463-102">SYNOPSIS</span></span>
<span data-ttu-id="f8463-103">Usuwa regułę alertu metryki v2 (nie klasyczna).</span><span class="sxs-lookup"><span data-stu-id="f8463-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="f8463-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8463-104">SYNTAX</span></span>

### <span data-ttu-id="f8463-105">ByMetricRuleResourceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8463-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8463-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="f8463-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8463-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="f8463-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8463-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f8463-108">DESCRIPTION</span></span>
<span data-ttu-id="f8463-109">Polecenie cmdlet **Remove-AzMetricAlertRuleV2** umożliwia usunięcie reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="f8463-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="f8463-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="f8463-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f8463-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8463-111">EXAMPLES</span></span>

### <span data-ttu-id="f8463-112">Przykład 1: Usuwanie reguły alertu według nazwy</span><span class="sxs-lookup"><span data-stu-id="f8463-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="f8463-113">To polecenie usuwa regułę alertu o nazwie PsSdk</span><span class="sxs-lookup"><span data-stu-id="f8463-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="f8463-114">Przykład 2: Usuwanie reguły alertu według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="f8463-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="f8463-115">To polecenie usuwa regułę alertu z IDENTYFIKATORem zasobu `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="f8463-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="f8463-116">Przykład 3: otrzymywanie alertu i usuwanie go</span><span class="sxs-lookup"><span data-stu-id="f8463-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="f8463-117">To polecenie pobiera alert i usuwa go.</span><span class="sxs-lookup"><span data-stu-id="f8463-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="f8463-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8463-118">PARAMETERS</span></span>

### <span data-ttu-id="f8463-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8463-119">-AsJob</span></span>
<span data-ttu-id="f8463-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f8463-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8463-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8463-121">-DefaultProfile</span></span>
<span data-ttu-id="f8463-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8463-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8463-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8463-123">-InputObject</span></span>
<span data-ttu-id="f8463-124">Obiekt reguły metryki</span><span class="sxs-lookup"><span data-stu-id="f8463-124">The Metric rule object</span></span>

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

### <span data-ttu-id="f8463-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8463-125">-Name</span></span>
<span data-ttu-id="f8463-126">Nazwa reguły alertu metryki</span><span class="sxs-lookup"><span data-stu-id="f8463-126">The name of metric alert rule</span></span>

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

### <span data-ttu-id="f8463-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8463-127">-PassThru</span></span>
<span data-ttu-id="f8463-128">Zwraca wartość Prawda po udanym usunięciu.</span><span class="sxs-lookup"><span data-stu-id="f8463-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="f8463-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8463-129">-ResourceGroupName</span></span>
<span data-ttu-id="f8463-130">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8463-130">The ResourceGroupName</span></span>

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

### <span data-ttu-id="f8463-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8463-131">-ResourceId</span></span>
<span data-ttu-id="f8463-132">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="f8463-132">The RuleResourceId</span></span>

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

### <span data-ttu-id="f8463-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8463-133">-Confirm</span></span>
<span data-ttu-id="f8463-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8463-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8463-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8463-135">-WhatIf</span></span>
<span data-ttu-id="f8463-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8463-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8463-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8463-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8463-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8463-138">CommonParameters</span></span>
<span data-ttu-id="f8463-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8463-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8463-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8463-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8463-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8463-141">INPUTS</span></span>

### <span data-ttu-id="f8463-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f8463-142">System.String</span></span>

### <span data-ttu-id="f8463-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f8463-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="f8463-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8463-144">OUTPUTS</span></span>

### <span data-ttu-id="f8463-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8463-145">System.Boolean</span></span>

## <span data-ttu-id="f8463-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8463-146">NOTES</span></span>

## <span data-ttu-id="f8463-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8463-147">RELATED LINKS</span></span>

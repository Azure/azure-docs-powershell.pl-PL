---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180106"
---
# <span data-ttu-id="f5e9c-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f5e9c-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="f5e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e9c-103">Usuwa metryczną regułę alertów V2 (nieistnieczną).</span><span class="sxs-lookup"><span data-stu-id="f5e9c-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="f5e9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5e9c-104">SYNTAX</span></span>

### <span data-ttu-id="f5e9c-105">ByMetricRuleResourceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f5e9c-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e9c-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e9c-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e9c-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="f5e9c-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5e9c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5e9c-108">DESCRIPTION</span></span>
<span data-ttu-id="f5e9c-109">Polecenie **cmdlet Remove-AzMetricAlertRuleV2** usuwa regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="f5e9c-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed jego utworzeniem, zmodyfikowaniem lub usunięciem.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f5e9c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5e9c-111">EXAMPLES</span></span>

### <span data-ttu-id="f5e9c-112">Przykład 1. Usuwanie reguły alertu według nazwy</span><span class="sxs-lookup"><span data-stu-id="f5e9c-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="f5e9c-113">To polecenie usuwa regułę alertu o nazwie PsSdk</span><span class="sxs-lookup"><span data-stu-id="f5e9c-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="f5e9c-114">Przykład 2. Usuwanie reguły alertu według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="f5e9c-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="f5e9c-115">To polecenie usuwa regułę alertu z identyfikatorem zasobu `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="f5e9c-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="f5e9c-116">Przykład 3. Uzyskiwanie alertu i usuwanie go</span><span class="sxs-lookup"><span data-stu-id="f5e9c-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="f5e9c-117">To polecenie pobiera alert i usuwa go.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="f5e9c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5e9c-118">PARAMETERS</span></span>

### <span data-ttu-id="f5e9c-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f5e9c-119">-AsJob</span></span>
<span data-ttu-id="f5e9c-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f5e9c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5e9c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e9c-121">-DefaultProfile</span></span>
<span data-ttu-id="f5e9c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e9c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5e9c-123">-InputObject</span></span>
<span data-ttu-id="f5e9c-124">Obiekt Reguły metryczne</span><span class="sxs-lookup"><span data-stu-id="f5e9c-124">The Metric rule object</span></span>

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

### <span data-ttu-id="f5e9c-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5e9c-125">-Name</span></span>
<span data-ttu-id="f5e9c-126">Nazwa reguły alertu metryczne</span><span class="sxs-lookup"><span data-stu-id="f5e9c-126">The name of metric alert rule</span></span>

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

### <span data-ttu-id="f5e9c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5e9c-127">-PassThru</span></span>
<span data-ttu-id="f5e9c-128">Zwróć wartość true po pomyślnym usunięciu.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="f5e9c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e9c-129">-ResourceGroupName</span></span>
<span data-ttu-id="f5e9c-130">The ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e9c-130">The ResourceGroupName</span></span>

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

### <span data-ttu-id="f5e9c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e9c-131">-ResourceId</span></span>
<span data-ttu-id="f5e9c-132">The RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e9c-132">The RuleResourceId</span></span>

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

### <span data-ttu-id="f5e9c-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5e9c-133">-Confirm</span></span>
<span data-ttu-id="f5e9c-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e9c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e9c-135">-WhatIf</span></span>
<span data-ttu-id="f5e9c-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5e9c-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e9c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e9c-138">CommonParameters</span></span>
<span data-ttu-id="f5e9c-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e9c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e9c-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5e9c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e9c-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5e9c-141">INPUTS</span></span>

### <span data-ttu-id="f5e9c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f5e9c-142">System.String</span></span>

### <span data-ttu-id="f5e9c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f5e9c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="f5e9c-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5e9c-144">OUTPUTS</span></span>

### <span data-ttu-id="f5e9c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5e9c-145">System.Boolean</span></span>

## <span data-ttu-id="f5e9c-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5e9c-146">NOTES</span></span>

## <span data-ttu-id="f5e9c-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5e9c-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 27fb22a5cded5e196a4bef0aa8b504771abef864
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998264"
---
# <span data-ttu-id="a0509-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="a0509-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="a0509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0509-102">SYNOPSIS</span></span>
<span data-ttu-id="a0509-103">Pobiera informacje podsumowujące alerty</span><span class="sxs-lookup"><span data-stu-id="a0509-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="a0509-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0509-104">SYNTAX</span></span>

### <span data-ttu-id="a0509-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="a0509-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0509-106">Filtr podsumowania</span><span class="sxs-lookup"><span data-stu-id="a0509-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0509-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0509-107">DESCRIPTION</span></span>
<span data-ttu-id="a0509-108">**Polecenie cmdlet Measure-AzAlertStatistic** pobiera szczegóły podsumowania alertu.</span><span class="sxs-lookup"><span data-stu-id="a0509-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="a0509-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0509-109">EXAMPLES</span></span>

### <span data-ttu-id="a0509-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0509-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="a0509-111">Podsumowuje liczbę alertów pogrupowanych według ważności i stanu filtrowanych według stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="a0509-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="a0509-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0509-112">PARAMETERS</span></span>

### <span data-ttu-id="a0509-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a0509-113">-AlertRuleId</span></span>
<span data-ttu-id="a0509-114">Filtruj według identyfikatora reguły alertu</span><span class="sxs-lookup"><span data-stu-id="a0509-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="a0509-115">- CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="a0509-115">-CustomTimeRange</span></span>
<span data-ttu-id="a0509-116">Obsługiwany format — \<start-time\> / \<end-time\> tam, gdzie czas jest w formacie ISO-8601</span><span class="sxs-lookup"><span data-stu-id="a0509-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="a0509-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0509-117">-DefaultProfile</span></span>
<span data-ttu-id="a0509-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0509-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0509-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="a0509-119">-GroupBy</span></span>
<span data-ttu-id="a0509-120">Właściwość Summarize by</span><span class="sxs-lookup"><span data-stu-id="a0509-120">Summarize by property</span></span>

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

### <span data-ttu-id="a0509-121">- IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="a0509-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="a0509-122">Uwzględnianie liczby grup inteligentnych</span><span class="sxs-lookup"><span data-stu-id="a0509-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0509-123">- MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="a0509-123">-MonitorCondition</span></span>
<span data-ttu-id="a0509-124">Filtruj według warunku monitora</span><span class="sxs-lookup"><span data-stu-id="a0509-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="a0509-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="a0509-125">-MonitorService</span></span>
<span data-ttu-id="a0509-126">Filtr w usłudze Moniter</span><span class="sxs-lookup"><span data-stu-id="a0509-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="a0509-127">— Ważność</span><span class="sxs-lookup"><span data-stu-id="a0509-127">-Severity</span></span>
<span data-ttu-id="a0509-128">Filtruj według ważności alertu</span><span class="sxs-lookup"><span data-stu-id="a0509-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="a0509-129">— województwo</span><span class="sxs-lookup"><span data-stu-id="a0509-129">-State</span></span>
<span data-ttu-id="a0509-130">Filtrowanie według stanu alertu</span><span class="sxs-lookup"><span data-stu-id="a0509-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="a0509-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0509-131">-TargetResourceGroup</span></span>
<span data-ttu-id="a0509-132">Filtruj według nazwy grupy zasobów docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="a0509-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0509-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a0509-133">-TargetResourceId</span></span>
<span data-ttu-id="a0509-134">Filtruj według identyfikatora zasobu docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="a0509-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0509-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="a0509-135">-TargetResourceType</span></span>
<span data-ttu-id="a0509-136">Filtruj według typu zasobu docelowego alertu.</span><span class="sxs-lookup"><span data-stu-id="a0509-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0509-137">- TimeRange</span><span class="sxs-lookup"><span data-stu-id="a0509-137">-TimeRange</span></span>
<span data-ttu-id="a0509-138">Obsługiwane wartości zakresu czasu — 1h, 1d, 7d, 30d (wartość domyślna to 1d)</span><span class="sxs-lookup"><span data-stu-id="a0509-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="a0509-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0509-139">CommonParameters</span></span>
<span data-ttu-id="a0509-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0509-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0509-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0509-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0509-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0509-142">INPUTS</span></span>

### <span data-ttu-id="a0509-143">Brak</span><span class="sxs-lookup"><span data-stu-id="a0509-143">None</span></span>

## <span data-ttu-id="a0509-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0509-144">OUTPUTS</span></span>

### <span data-ttu-id="a0509-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="a0509-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="a0509-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0509-146">NOTES</span></span>

## <span data-ttu-id="a0509-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0509-147">RELATED LINKS</span></span>

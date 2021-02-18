---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239963"
---
# <span data-ttu-id="bc6a9-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="bc6a9-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="bc6a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6a9-103">Pobiera informacje podsumowujące alerty</span><span class="sxs-lookup"><span data-stu-id="bc6a9-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="bc6a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc6a9-104">SYNTAX</span></span>

### <span data-ttu-id="bc6a9-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="bc6a9-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc6a9-106">Filtr podsumowania</span><span class="sxs-lookup"><span data-stu-id="bc6a9-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc6a9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc6a9-107">DESCRIPTION</span></span>
<span data-ttu-id="bc6a9-108">**Polecenie cmdlet Measure-AzAlertStatistic** pobiera szczegóły podsumowania alertu.</span><span class="sxs-lookup"><span data-stu-id="bc6a9-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="bc6a9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc6a9-109">EXAMPLES</span></span>

### <span data-ttu-id="bc6a9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc6a9-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="bc6a9-111">Podsumowuje liczbę alertów pogrupowanych według ważności i stanu filtrowanych według stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="bc6a9-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="bc6a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc6a9-112">PARAMETERS</span></span>

### <span data-ttu-id="bc6a9-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="bc6a9-113">-AlertRuleId</span></span>
<span data-ttu-id="bc6a9-114">Filtruj według identyfikatora reguły alertu</span><span class="sxs-lookup"><span data-stu-id="bc6a9-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="bc6a9-115">- CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="bc6a9-115">-CustomTimeRange</span></span>
<span data-ttu-id="bc6a9-116">Obsługiwany format — \<start-time\> / \<end-time\> tam, gdzie czas jest w formacie ISO-8601</span><span class="sxs-lookup"><span data-stu-id="bc6a9-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="bc6a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6a9-117">-DefaultProfile</span></span>
<span data-ttu-id="bc6a9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc6a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc6a9-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="bc6a9-119">-GroupBy</span></span>
<span data-ttu-id="bc6a9-120">Właściwość Summarize by</span><span class="sxs-lookup"><span data-stu-id="bc6a9-120">Summarize by property</span></span>

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

### <span data-ttu-id="bc6a9-121">- IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="bc6a9-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="bc6a9-122">Uwzględnianie liczby grup inteligentnych</span><span class="sxs-lookup"><span data-stu-id="bc6a9-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="bc6a9-123">- MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="bc6a9-123">-MonitorCondition</span></span>
<span data-ttu-id="bc6a9-124">Filtruj według warunku monitora</span><span class="sxs-lookup"><span data-stu-id="bc6a9-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="bc6a9-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="bc6a9-125">-MonitorService</span></span>
<span data-ttu-id="bc6a9-126">Filtr w usłudze Moniter</span><span class="sxs-lookup"><span data-stu-id="bc6a9-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="bc6a9-127">— Ważność</span><span class="sxs-lookup"><span data-stu-id="bc6a9-127">-Severity</span></span>
<span data-ttu-id="bc6a9-128">Filtruj według ważności alertu</span><span class="sxs-lookup"><span data-stu-id="bc6a9-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="bc6a9-129">— województwo</span><span class="sxs-lookup"><span data-stu-id="bc6a9-129">-State</span></span>
<span data-ttu-id="bc6a9-130">Filtrowanie według stanu alertu</span><span class="sxs-lookup"><span data-stu-id="bc6a9-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="bc6a9-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bc6a9-131">-TargetResourceGroup</span></span>
<span data-ttu-id="bc6a9-132">Filtruj według nazwy grupy zasobów docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="bc6a9-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="bc6a9-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bc6a9-133">-TargetResourceId</span></span>
<span data-ttu-id="bc6a9-134">Filtruj według identyfikatora zasobu docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="bc6a9-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="bc6a9-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="bc6a9-135">-TargetResourceType</span></span>
<span data-ttu-id="bc6a9-136">Filtruj według typu zasobu docelowego alertu.</span><span class="sxs-lookup"><span data-stu-id="bc6a9-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="bc6a9-137">- TimeRange</span><span class="sxs-lookup"><span data-stu-id="bc6a9-137">-TimeRange</span></span>
<span data-ttu-id="bc6a9-138">Obsługiwane wartości zakresu czasu — 1h, 1d, 7d, 30d (wartość domyślna to 1d)</span><span class="sxs-lookup"><span data-stu-id="bc6a9-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="bc6a9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6a9-139">CommonParameters</span></span>
<span data-ttu-id="bc6a9-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc6a9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6a9-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc6a9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6a9-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc6a9-142">INPUTS</span></span>

### <span data-ttu-id="bc6a9-143">Brak</span><span class="sxs-lookup"><span data-stu-id="bc6a9-143">None</span></span>

## <span data-ttu-id="bc6a9-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc6a9-144">OUTPUTS</span></span>

### <span data-ttu-id="bc6a9-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="bc6a9-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="bc6a9-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc6a9-146">NOTES</span></span>

## <span data-ttu-id="bc6a9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc6a9-147">RELATED LINKS</span></span>

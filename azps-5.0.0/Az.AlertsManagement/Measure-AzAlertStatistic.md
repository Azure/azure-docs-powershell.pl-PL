---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224601"
---
# <span data-ttu-id="ada59-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="ada59-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="ada59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ada59-102">SYNOPSIS</span></span>
<span data-ttu-id="ada59-103">Pobiera informacje podsumowujące alert</span><span class="sxs-lookup"><span data-stu-id="ada59-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="ada59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ada59-104">SYNTAX</span></span>

### <span data-ttu-id="ada59-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="ada59-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ada59-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="ada59-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada59-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ada59-107">DESCRIPTION</span></span>
<span data-ttu-id="ada59-108">**Measure-** polecenie cmdlet AzAlertStatistic pobiera szczegóły podsumowania alertu.</span><span class="sxs-lookup"><span data-stu-id="ada59-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="ada59-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ada59-109">EXAMPLES</span></span>

### <span data-ttu-id="ada59-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ada59-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="ada59-111">Podsumowanie liczby alertów pogrupowanych według ważności i stanu filtrowanych według stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="ada59-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="ada59-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ada59-112">PARAMETERS</span></span>

### <span data-ttu-id="ada59-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="ada59-113">-AlertRuleId</span></span>
<span data-ttu-id="ada59-114">Filtrowanie według identyfikatora reguły alertu</span><span class="sxs-lookup"><span data-stu-id="ada59-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="ada59-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="ada59-115">-CustomTimeRange</span></span>
<span data-ttu-id="ada59-116">Obsługiwany format — \<start-time\> / \<end-time\> gdy czas jest w formacie ISO-8601</span><span class="sxs-lookup"><span data-stu-id="ada59-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="ada59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada59-117">-DefaultProfile</span></span>
<span data-ttu-id="ada59-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ada59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada59-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="ada59-119">-GroupBy</span></span>
<span data-ttu-id="ada59-120">Podsumowanie według właściwości</span><span class="sxs-lookup"><span data-stu-id="ada59-120">Summarize by property</span></span>

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

### <span data-ttu-id="ada59-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="ada59-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="ada59-122">Uwzględnij zliczanie SmartGroups</span><span class="sxs-lookup"><span data-stu-id="ada59-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="ada59-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="ada59-123">-MonitorCondition</span></span>
<span data-ttu-id="ada59-124">Filtr na stanie monitora</span><span class="sxs-lookup"><span data-stu-id="ada59-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="ada59-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="ada59-125">-MonitorService</span></span>
<span data-ttu-id="ada59-126">Filtrowanie w usłudze moniter</span><span class="sxs-lookup"><span data-stu-id="ada59-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="ada59-127">— Ważność</span><span class="sxs-lookup"><span data-stu-id="ada59-127">-Severity</span></span>
<span data-ttu-id="ada59-128">Filtrowanie według dotkliwości alertu</span><span class="sxs-lookup"><span data-stu-id="ada59-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="ada59-129">-State</span><span class="sxs-lookup"><span data-stu-id="ada59-129">-State</span></span>
<span data-ttu-id="ada59-130">Filtrowanie w stanie alertu</span><span class="sxs-lookup"><span data-stu-id="ada59-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="ada59-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ada59-131">-TargetResourceGroup</span></span>
<span data-ttu-id="ada59-132">Filtruj według nazwy grupy zasobów dla zasobu docelowego alertu.</span><span class="sxs-lookup"><span data-stu-id="ada59-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="ada59-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ada59-133">-TargetResourceId</span></span>
<span data-ttu-id="ada59-134">Filtrowanie identyfikatora zasobu dla docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="ada59-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="ada59-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="ada59-135">-TargetResourceType</span></span>
<span data-ttu-id="ada59-136">Filtrowanie według typu zasobu docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="ada59-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="ada59-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="ada59-137">-TimeRange</span></span>
<span data-ttu-id="ada59-138">Obsługiwane wartości zakresu czasu — 1H, 1D, 7D, 30d (wartość domyślna to 1D)</span><span class="sxs-lookup"><span data-stu-id="ada59-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="ada59-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada59-139">CommonParameters</span></span>
<span data-ttu-id="ada59-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada59-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada59-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ada59-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada59-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada59-142">INPUTS</span></span>

### <span data-ttu-id="ada59-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ada59-143">None</span></span>

## <span data-ttu-id="ada59-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ada59-144">OUTPUTS</span></span>

### <span data-ttu-id="ada59-145">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="ada59-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="ada59-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ada59-146">NOTES</span></span>

## <span data-ttu-id="ada59-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ada59-147">RELATED LINKS</span></span>

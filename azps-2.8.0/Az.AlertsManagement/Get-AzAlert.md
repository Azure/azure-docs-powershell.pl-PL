---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: e3a5cbe95bf524a70194cfce7e0b8bb80b701dec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707156"
---
# <span data-ttu-id="0a4e0-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="0a4e0-101">Get-AzAlert</span></span>

## <span data-ttu-id="0a4e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a4e0-103">Uzyskiwanie informacji o alertach</span><span class="sxs-lookup"><span data-stu-id="0a4e0-103">Get Alerts Information</span></span>

## <span data-ttu-id="0a4e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a4e0-104">SYNTAX</span></span>

### <span data-ttu-id="0a4e0-105">AlertsListByFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a4e0-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a4e0-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="0a4e0-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a4e0-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="0a4e0-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a4e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0a4e0-108">DESCRIPTION</span></span>
<span data-ttu-id="0a4e0-109">Polecenie cmdlet **Get-AzAlert** umożliwia wygenerowane wystąpienia alertów.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="0a4e0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a4e0-110">EXAMPLES</span></span>

### <span data-ttu-id="0a4e0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0a4e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="0a4e0-112">Lista wszystkich alertów o ważności Sev2 oraz stan monitora.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="0a4e0-113">Ustawienie IncludeContext na wartość true, dołączanie niestandardowego ładunku alertu.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="0a4e0-114">Użyj Format-List, aby uzyskać pełne szczegóły poszczególnych alertów na liście.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="0a4e0-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0a4e0-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="0a4e0-116">Uzyskiwanie szczegółowych informacji o alercie według identyfikatora (GUID) lub identyfikatora zasobu (pełna nazwa RAMIENIa)</span><span class="sxs-lookup"><span data-stu-id="0a4e0-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="0a4e0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a4e0-117">PARAMETERS</span></span>

### <span data-ttu-id="0a4e0-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="0a4e0-118">-AlertId</span></span>
<span data-ttu-id="0a4e0-119">Unikatowy identyfikator alertu/ResourceId alertu.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0a4e0-120">-AlertRuleId</span></span>
<span data-ttu-id="0a4e0-121">Filtrowanie według identyfikatora reguły alertu</span><span class="sxs-lookup"><span data-stu-id="0a4e0-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="0a4e0-122">-CustomTimeRange</span></span>
<span data-ttu-id="0a4e0-123">Obsługiwany format — \< \> / \< czas zakończenia w czasie końcowym, \> gdy czas jest w formacie ISO-8601</span><span class="sxs-lookup"><span data-stu-id="0a4e0-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4e0-124">-DefaultProfile</span></span>
<span data-ttu-id="0a4e0-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a4e0-126">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="0a4e0-126">-IncludeContext</span></span>
<span data-ttu-id="0a4e0-127">Uwzględnij kontekst (ładunek niestandardowy) alertu</span><span class="sxs-lookup"><span data-stu-id="0a4e0-127">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="0a4e0-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="0a4e0-129">Uwzględnij EgressConfig</span><span class="sxs-lookup"><span data-stu-id="0a4e0-129">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="0a4e0-130">-MonitorCondition</span></span>
<span data-ttu-id="0a4e0-131">Filtr na stanie monitora</span><span class="sxs-lookup"><span data-stu-id="0a4e0-131">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="0a4e0-132">-MonitorService</span></span>
<span data-ttu-id="0a4e0-133">Filtrowanie w usłudze moniter</span><span class="sxs-lookup"><span data-stu-id="0a4e0-133">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="0a4e0-134">-PageCount</span></span>
<span data-ttu-id="0a4e0-135">Liczba alertów, które mają zostać pobrane na stronie.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-135">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-136">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="0a4e0-136">-Select</span></span>
<span data-ttu-id="0a4e0-137">Zaprojektuj wymagane pola poza programem Essentials.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="0a4e0-138">Oczekiwane dane wejściowe są rozdzielane przecinkami.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-138">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-139">— Ważność</span><span class="sxs-lookup"><span data-stu-id="0a4e0-139">-Severity</span></span>
<span data-ttu-id="0a4e0-140">Filtrowanie według dotkliwości alertu</span><span class="sxs-lookup"><span data-stu-id="0a4e0-140">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="0a4e0-141">-SmartGroupId</span></span>
<span data-ttu-id="0a4e0-142">Filtrowanie wszystkich alertów o identyfikatorze grupy inteligentnej</span><span class="sxs-lookup"><span data-stu-id="0a4e0-142">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-143">-SortBy</span><span class="sxs-lookup"><span data-stu-id="0a4e0-143">-SortBy</span></span>
<span data-ttu-id="0a4e0-144">Właściwość alertu używana podczas sortowania</span><span class="sxs-lookup"><span data-stu-id="0a4e0-144">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="0a4e0-145">-SortOrder</span></span>
<span data-ttu-id="0a4e0-146">Kolejność sortowania</span><span class="sxs-lookup"><span data-stu-id="0a4e0-146">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-147">-State</span><span class="sxs-lookup"><span data-stu-id="0a4e0-147">-State</span></span>
<span data-ttu-id="0a4e0-148">Filtrowanie w stanie alertu</span><span class="sxs-lookup"><span data-stu-id="0a4e0-148">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a4e0-149">-TargetResourceGroup</span></span>
<span data-ttu-id="0a4e0-150">Filtruj według nazwy grupy zasobów dla zasobu docelowego alertu.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-150">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0a4e0-151">-TargetResourceId</span></span>
<span data-ttu-id="0a4e0-152">Filtrowanie identyfikatora zasobu dla docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-152">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="0a4e0-153">-TargetResourceType</span></span>
<span data-ttu-id="0a4e0-154">Filtrowanie według typu zasobu docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-154">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="0a4e0-155">-TimeRange</span></span>
<span data-ttu-id="0a4e0-156">Obsługiwane wartości zakresu czasu — 1H, 1D, 7D, 30d (wartość domyślna to 1D)</span><span class="sxs-lookup"><span data-stu-id="0a4e0-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a4e0-157">CommonParameters</span></span>
<span data-ttu-id="0a4e0-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a4e0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a4e0-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a4e0-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a4e0-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a4e0-160">INPUTS</span></span>

### <span data-ttu-id="0a4e0-161">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0a4e0-161">None</span></span>

## <span data-ttu-id="0a4e0-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a4e0-162">OUTPUTS</span></span>

### <span data-ttu-id="0a4e0-163">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="0a4e0-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="0a4e0-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a4e0-164">NOTES</span></span>

## <span data-ttu-id="0a4e0-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a4e0-165">RELATED LINKS</span></span>

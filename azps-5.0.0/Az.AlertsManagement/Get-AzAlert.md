---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319399"
---
# <span data-ttu-id="f8ba9-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="f8ba9-101">Get-AzAlert</span></span>

## <span data-ttu-id="f8ba9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ba9-103">Uzyskiwanie informacji o alertach</span><span class="sxs-lookup"><span data-stu-id="f8ba9-103">Get Alerts Information</span></span>

## <span data-ttu-id="f8ba9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8ba9-104">SYNTAX</span></span>

### <span data-ttu-id="f8ba9-105">AlertsListByFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8ba9-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="f8ba9-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8ba9-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="f8ba9-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8ba9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f8ba9-108">DESCRIPTION</span></span>
<span data-ttu-id="f8ba9-109">Polecenie cmdlet **Get-AzAlert** umożliwia wygenerowane wystąpienia alertów.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="f8ba9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8ba9-110">EXAMPLES</span></span>

### <span data-ttu-id="f8ba9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f8ba9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="f8ba9-112">Lista wszystkich alertów o ważności Sev2 oraz stan monitora.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="f8ba9-113">Ustawienie IncludeContext na wartość true, dołączanie niestandardowego ładunku alertu.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="f8ba9-114">Użyj Format-List, aby uzyskać pełne szczegóły poszczególnych alertów na liście.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="f8ba9-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f8ba9-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="f8ba9-116">Uzyskiwanie szczegółowych informacji o alercie według identyfikatora (GUID) lub identyfikatora zasobu (pełna nazwa RAMIENIa)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="f8ba9-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f8ba9-117">Example 3</span></span>

<span data-ttu-id="f8ba9-118">Uzyskiwanie informacji o alertach.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-118">Get Alerts Information.</span></span> <span data-ttu-id="f8ba9-119">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="f8ba9-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8ba9-120">PARAMETERS</span></span>

### <span data-ttu-id="f8ba9-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="f8ba9-121">-AlertId</span></span>
<span data-ttu-id="f8ba9-122">Unikatowy identyfikator alertu/ResourceId alertu.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="f8ba9-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="f8ba9-123">-AlertRuleId</span></span>
<span data-ttu-id="f8ba9-124">Filtrowanie według identyfikatora reguły alertu</span><span class="sxs-lookup"><span data-stu-id="f8ba9-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="f8ba9-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="f8ba9-125">-CustomTimeRange</span></span>
<span data-ttu-id="f8ba9-126">Obsługiwany format — \<start-time\> / \<end-time\> gdy czas jest w formacie ISO-8601</span><span class="sxs-lookup"><span data-stu-id="f8ba9-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="f8ba9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ba9-127">-DefaultProfile</span></span>
<span data-ttu-id="f8ba9-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8ba9-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="f8ba9-129">-IncludeContext</span></span>
<span data-ttu-id="f8ba9-130">Uwzględnij kontekst (ładunek niestandardowy) alertu</span><span class="sxs-lookup"><span data-stu-id="f8ba9-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="f8ba9-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="f8ba9-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="f8ba9-132">Uwzględnij EgressConfig</span><span class="sxs-lookup"><span data-stu-id="f8ba9-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="f8ba9-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="f8ba9-133">-MonitorCondition</span></span>
<span data-ttu-id="f8ba9-134">Filtr na stanie monitora</span><span class="sxs-lookup"><span data-stu-id="f8ba9-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="f8ba9-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="f8ba9-135">-MonitorService</span></span>
<span data-ttu-id="f8ba9-136">Filtrowanie w usłudze moniter</span><span class="sxs-lookup"><span data-stu-id="f8ba9-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="f8ba9-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="f8ba9-137">-PageCount</span></span>
<span data-ttu-id="f8ba9-138">Liczba alertów, które mają zostać pobrane na stronie.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="f8ba9-139">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="f8ba9-139">-Select</span></span>
<span data-ttu-id="f8ba9-140">Zaprojektuj wymagane pola poza programem Essentials.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="f8ba9-141">Oczekiwane dane wejściowe są rozdzielane przecinkami.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="f8ba9-142">— Ważność</span><span class="sxs-lookup"><span data-stu-id="f8ba9-142">-Severity</span></span>
<span data-ttu-id="f8ba9-143">Filtrowanie według dotkliwości alertu</span><span class="sxs-lookup"><span data-stu-id="f8ba9-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="f8ba9-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="f8ba9-144">-SmartGroupId</span></span>
<span data-ttu-id="f8ba9-145">Filtrowanie wszystkich alertów o identyfikatorze grupy inteligentnej</span><span class="sxs-lookup"><span data-stu-id="f8ba9-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="f8ba9-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="f8ba9-146">-SortBy</span></span>
<span data-ttu-id="f8ba9-147">Właściwość alertu używana podczas sortowania</span><span class="sxs-lookup"><span data-stu-id="f8ba9-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="f8ba9-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="f8ba9-148">-SortOrder</span></span>
<span data-ttu-id="f8ba9-149">Kolejność sortowania</span><span class="sxs-lookup"><span data-stu-id="f8ba9-149">Sort Order</span></span>

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

### <span data-ttu-id="f8ba9-150">-State</span><span class="sxs-lookup"><span data-stu-id="f8ba9-150">-State</span></span>
<span data-ttu-id="f8ba9-151">Filtrowanie w stanie alertu</span><span class="sxs-lookup"><span data-stu-id="f8ba9-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="f8ba9-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8ba9-152">-TargetResourceGroup</span></span>
<span data-ttu-id="f8ba9-153">Filtruj według nazwy grupy zasobów dla zasobu docelowego alertu.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="f8ba9-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f8ba9-154">-TargetResourceId</span></span>
<span data-ttu-id="f8ba9-155">Filtrowanie identyfikatora zasobu dla docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="f8ba9-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="f8ba9-156">-TargetResourceType</span></span>
<span data-ttu-id="f8ba9-157">Filtrowanie według typu zasobu docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="f8ba9-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="f8ba9-158">-TimeRange</span></span>
<span data-ttu-id="f8ba9-159">Obsługiwane wartości zakresu czasu — 1H, 1D, 7D, 30d (wartość domyślna to 1D)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="f8ba9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ba9-160">CommonParameters</span></span>
<span data-ttu-id="f8ba9-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ba9-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8ba9-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ba9-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8ba9-163">INPUTS</span></span>

### <span data-ttu-id="f8ba9-164">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f8ba9-164">None</span></span>

## <span data-ttu-id="f8ba9-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8ba9-165">OUTPUTS</span></span>

### <span data-ttu-id="f8ba9-166">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="f8ba9-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="f8ba9-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8ba9-167">NOTES</span></span>

## <span data-ttu-id="f8ba9-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8ba9-168">RELATED LINKS</span></span>

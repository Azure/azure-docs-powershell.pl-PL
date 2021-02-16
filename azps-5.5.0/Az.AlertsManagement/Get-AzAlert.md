---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199810"
---
# <span data-ttu-id="11d1a-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="11d1a-101">Get-AzAlert</span></span>

## <span data-ttu-id="11d1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="11d1a-103">Uzyskiwanie informacji o alertach</span><span class="sxs-lookup"><span data-stu-id="11d1a-103">Get Alerts Information</span></span>

## <span data-ttu-id="11d1a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11d1a-104">SYNTAX</span></span>

### <span data-ttu-id="11d1a-105">AlertsListByFilter (domyślne)</span><span class="sxs-lookup"><span data-stu-id="11d1a-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11d1a-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="11d1a-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11d1a-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="11d1a-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11d1a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="11d1a-108">DESCRIPTION</span></span>
<span data-ttu-id="11d1a-109">**Polecenie cmdlet Get-AzAlert** zostaje zwolnione w wystąpieniach alertów.</span><span class="sxs-lookup"><span data-stu-id="11d1a-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="11d1a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11d1a-110">EXAMPLES</span></span>

### <span data-ttu-id="11d1a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11d1a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="11d1a-112">Lista wszystkich alertów z poziomem ważności Sev2 i warunkiem monitorowania Odpalone.</span><span class="sxs-lookup"><span data-stu-id="11d1a-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="11d1a-113">Ustawienie wartości IncludeContext na prawda, uwzględnia niestandardowe obciążenie alertu.</span><span class="sxs-lookup"><span data-stu-id="11d1a-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="11d1a-114">Użyj Format-List, aby uzyskać pełne szczegóły każdego alertu na liście.</span><span class="sxs-lookup"><span data-stu-id="11d1a-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="11d1a-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11d1a-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="11d1a-116">Uzyskiwanie szczegółów alertu według identyfikatora (GUID) lub identyfikatora zasobu (identyfikator ARM danych)</span><span class="sxs-lookup"><span data-stu-id="11d1a-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="11d1a-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="11d1a-117">Example 3</span></span>

<span data-ttu-id="11d1a-118">Uzyskiwanie informacji o alertach.</span><span class="sxs-lookup"><span data-stu-id="11d1a-118">Get Alerts Information.</span></span> <span data-ttu-id="11d1a-119">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="11d1a-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="11d1a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11d1a-120">PARAMETERS</span></span>

### <span data-ttu-id="11d1a-121">- AlertId</span><span class="sxs-lookup"><span data-stu-id="11d1a-121">-AlertId</span></span>
<span data-ttu-id="11d1a-122">Unikatowy identyfikator alertu/identyfikatora zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="11d1a-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="11d1a-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="11d1a-123">-AlertRuleId</span></span>
<span data-ttu-id="11d1a-124">Filtruj według identyfikatora reguły alertu</span><span class="sxs-lookup"><span data-stu-id="11d1a-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="11d1a-125">- CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="11d1a-125">-CustomTimeRange</span></span>
<span data-ttu-id="11d1a-126">Obsługiwany format — \<start-time\> / \<end-time\> tam, gdzie czas jest w formacie ISO-8601</span><span class="sxs-lookup"><span data-stu-id="11d1a-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="11d1a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d1a-127">-DefaultProfile</span></span>
<span data-ttu-id="11d1a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11d1a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d1a-129">- IncludeContext</span><span class="sxs-lookup"><span data-stu-id="11d1a-129">-IncludeContext</span></span>
<span data-ttu-id="11d1a-130">Uwzględnianie kontekstu (niestandardowego ładu) alertu</span><span class="sxs-lookup"><span data-stu-id="11d1a-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="11d1a-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="11d1a-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="11d1a-132">Uwzględnij konfigurację poczty wychodzącej</span><span class="sxs-lookup"><span data-stu-id="11d1a-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="11d1a-133">- MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="11d1a-133">-MonitorCondition</span></span>
<span data-ttu-id="11d1a-134">Filtruj według warunku monitora</span><span class="sxs-lookup"><span data-stu-id="11d1a-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="11d1a-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="11d1a-135">-MonitorService</span></span>
<span data-ttu-id="11d1a-136">Filtr w usłudze Moniter</span><span class="sxs-lookup"><span data-stu-id="11d1a-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="11d1a-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="11d1a-137">-PageCount</span></span>
<span data-ttu-id="11d1a-138">Liczba alertów do pobrania na stronie.</span><span class="sxs-lookup"><span data-stu-id="11d1a-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="11d1a-139">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="11d1a-139">-Select</span></span>
<span data-ttu-id="11d1a-140">Wyeksymuj wymagane pola poza podstawowymi elementami.</span><span class="sxs-lookup"><span data-stu-id="11d1a-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="11d1a-141">Oczekiwane dane wejściowe są oddzielone przecinkami.</span><span class="sxs-lookup"><span data-stu-id="11d1a-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="11d1a-142">— Ważność</span><span class="sxs-lookup"><span data-stu-id="11d1a-142">-Severity</span></span>
<span data-ttu-id="11d1a-143">Filtruj według ważności alertu</span><span class="sxs-lookup"><span data-stu-id="11d1a-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="11d1a-144">- SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="11d1a-144">-SmartGroupId</span></span>
<span data-ttu-id="11d1a-145">Filtrowanie wszystkich alertów z identyfikatorem grupy inteligentnej</span><span class="sxs-lookup"><span data-stu-id="11d1a-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="11d1a-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="11d1a-146">-SortBy</span></span>
<span data-ttu-id="11d1a-147">Właściwość alertu do użycia podczas sortowania</span><span class="sxs-lookup"><span data-stu-id="11d1a-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="11d1a-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="11d1a-148">-SortOrder</span></span>
<span data-ttu-id="11d1a-149">Porządek sortowania</span><span class="sxs-lookup"><span data-stu-id="11d1a-149">Sort Order</span></span>

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

### <span data-ttu-id="11d1a-150">— województwo</span><span class="sxs-lookup"><span data-stu-id="11d1a-150">-State</span></span>
<span data-ttu-id="11d1a-151">Filtrowanie według stanu alertu</span><span class="sxs-lookup"><span data-stu-id="11d1a-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="11d1a-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11d1a-152">-TargetResourceGroup</span></span>
<span data-ttu-id="11d1a-153">Filtruj według nazwy grupy zasobów docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="11d1a-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="11d1a-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="11d1a-154">-TargetResourceId</span></span>
<span data-ttu-id="11d1a-155">Filtruj według identyfikatora zasobu docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="11d1a-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="11d1a-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="11d1a-156">-TargetResourceType</span></span>
<span data-ttu-id="11d1a-157">Filtruj według typu zasobu docelowego alertu.</span><span class="sxs-lookup"><span data-stu-id="11d1a-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="11d1a-158">- TimeRange</span><span class="sxs-lookup"><span data-stu-id="11d1a-158">-TimeRange</span></span>
<span data-ttu-id="11d1a-159">Obsługiwane wartości zakresu czasu — 1h, 1d, 7d, 30d (wartość domyślna to 1d)</span><span class="sxs-lookup"><span data-stu-id="11d1a-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="11d1a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d1a-160">CommonParameters</span></span>
<span data-ttu-id="11d1a-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d1a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d1a-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11d1a-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d1a-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11d1a-163">INPUTS</span></span>

### <span data-ttu-id="11d1a-164">Brak</span><span class="sxs-lookup"><span data-stu-id="11d1a-164">None</span></span>

## <span data-ttu-id="11d1a-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11d1a-165">OUTPUTS</span></span>

### <span data-ttu-id="11d1a-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="11d1a-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="11d1a-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11d1a-167">NOTES</span></span>

## <span data-ttu-id="11d1a-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11d1a-168">RELATED LINKS</span></span>

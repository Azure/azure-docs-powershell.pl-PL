---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 1a0b2a4c66dba962518b9bb5ebca565f4bcd41bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708797"
---
# <span data-ttu-id="0ae24-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="0ae24-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="0ae24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ae24-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae24-103">Pobiera zdarzenia obliczania zasad generowane po utworzeniu lub zaktualizowaniu zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ae24-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="0ae24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ae24-104">SYNTAX</span></span>

### <span data-ttu-id="0ae24-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ae24-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ae24-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="0ae24-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ae24-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="0ae24-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ae24-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="0ae24-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ae24-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="0ae24-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ae24-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="0ae24-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ae24-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="0ae24-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ae24-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="0ae24-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ae24-113">Opis</span><span class="sxs-lookup"><span data-stu-id="0ae24-113">DESCRIPTION</span></span>
<span data-ttu-id="0ae24-114">Pobiera zdarzenia obliczania zasad generowane po utworzeniu lub zaktualizowaniu zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ae24-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="0ae24-115">Rekordy zdarzeń zasad mogą być badane w różnych zakresach na podstawie określonego interwału czasu (domyślnie do ostatniego dnia).</span><span class="sxs-lookup"><span data-stu-id="0ae24-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="0ae24-116">Wyniki mogą być filtrowane, grupowane, a agregacje grup mogą być obliczane.</span><span class="sxs-lookup"><span data-stu-id="0ae24-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="0ae24-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ae24-117">EXAMPLES</span></span>

### <span data-ttu-id="0ae24-118">Przykład 1: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="0ae24-119">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="0ae24-120">Przykład 2: pobieranie zdarzeń dotyczących zasad w określonym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="0ae24-121">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="0ae24-122">Przykład 3: pobieranie zdarzeń dotyczących zasad w zakresie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="0ae24-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="0ae24-123">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="0ae24-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="0ae24-124">Przykład 4: pobieranie zdarzeń dotyczących zasad w zakresie grupy zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="0ae24-125">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="0ae24-126">Przykład 5: pobieranie zdarzeń zasad w zakresie grupy zasobów w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="0ae24-127">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="0ae24-128">Przykład 6: pobieranie zdarzeń dotyczących zasad dla zasobu</span><span class="sxs-lookup"><span data-stu-id="0ae24-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="0ae24-129">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="0ae24-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="0ae24-130">Przykład 7: pobieranie zdarzeń dotyczących zasad dla definicji zestawu zasad w bieżącym abonamentzie</span><span class="sxs-lookup"><span data-stu-id="0ae24-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="0ae24-131">Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (istniejącej w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="0ae24-132">Przykład 8: pobieranie zdarzeń dotyczących zasad dla definicji zestawu zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="0ae24-133">Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (istniejącej w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="0ae24-134">Przykład 9: pobieranie zdarzeń dotyczących zasad dla definicji zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="0ae24-135">Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) zgodnie z określoną definicją zasad (istniejącą w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="0ae24-136">Przykład 10: pobieranie zdarzeń zasad dla definicji zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="0ae24-137">Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) zgodnie z określoną definicją zasad (istniejącą w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="0ae24-138">Przykład 11: pobieranie zdarzeń dotyczących zasad dla przypisania zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="0ae24-139">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) wykonywane przez określone przypisanie zasad (istniejące w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="0ae24-140">Przykład 12: pobieranie zdarzeń zasad dla przydziału zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="0ae24-141">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) dokonywanych przez określone przypisanie zasad (istniejące w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="0ae24-142">Przykład 13: pobieranie zdarzeń zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="0ae24-143">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych przez określone przypisanie zasad (istniejące w grupie zasobów w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="0ae24-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="0ae24-144">Przykład 14: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji OrderBy, początek i wybierz zapytanie</span><span class="sxs-lookup"><span data-stu-id="0ae24-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="0ae24-145">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="0ae24-146">Polecenie porządkuje wyniki według sygnatury czasowej i właściwości nazw przydziałów, a następnie pobiera tylko 5 najważniejszych osób z listy w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="0ae24-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="0ae24-147">Wybiera także listę tylko podzestawu kolumn dla każdego rekordu.</span><span class="sxs-lookup"><span data-stu-id="0ae24-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="0ae24-148">Przykład 15: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji od i do zapytania</span><span class="sxs-lookup"><span data-stu-id="0ae24-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="0ae24-149">Pobiera rekordy zdarzeń zasad wygenerowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="0ae24-150">Przykład 16: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji Filtruj zapytanie</span><span class="sxs-lookup"><span data-stu-id="0ae24-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="0ae24-151">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="0ae24-152">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (dotyczy to odmowy lub akcji inspekcji) oraz lokalizacji zasobów (z pominięciem lokalizacji wschodniego).</span><span class="sxs-lookup"><span data-stu-id="0ae24-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="0ae24-153">Przykład 17: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu Zastosuj Określanie agregacji liczby wierszy</span><span class="sxs-lookup"><span data-stu-id="0ae24-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="0ae24-154">Pobiera liczbę rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="0ae24-155">Polecenie zwraca liczbę tylko rekordów zdarzeń zasad, które są zwracane w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="0ae24-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="0ae24-156">Przykład 18: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu Zastosuj Określanie grupowania z agregacją</span><span class="sxs-lookup"><span data-stu-id="0ae24-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="0ae24-157">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="0ae24-158">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko zdarzenia inspekcji i Odmów).</span><span class="sxs-lookup"><span data-stu-id="0ae24-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="0ae24-159">Umożliwia grupowanie wyników na podstawie przydziału zasad, definicji zasad, akcji definicji zasad i identyfikatora zasobu oraz obliczanie liczby rekordów w każdej grupie, która jest zwracana w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="0ae24-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="0ae24-160">Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.</span><span class="sxs-lookup"><span data-stu-id="0ae24-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="0ae24-161">Przykład 19: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie grupowania bez agregacji</span><span class="sxs-lookup"><span data-stu-id="0ae24-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="0ae24-162">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="0ae24-163">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko zdarzenia inspekcji i Odmów).</span><span class="sxs-lookup"><span data-stu-id="0ae24-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="0ae24-164">Umożliwia grupowanie wyników na podstawie identyfikatora zasobu. Spowoduje to wygenerowanie listy wszystkich zasobów w ramach subskrypcji, które wygenerowały zdarzenie zasad dla co najmniej jednej inspekcji lub zasady odmowy.</span><span class="sxs-lookup"><span data-stu-id="0ae24-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="0ae24-165">Przykład 20: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie wielu grup</span><span class="sxs-lookup"><span data-stu-id="0ae24-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="0ae24-166">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="0ae24-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="0ae24-167">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (dotyczy tylko zdarzeń Odmów).</span><span class="sxs-lookup"><span data-stu-id="0ae24-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="0ae24-168">Najpierw grupuje wyniki na podstawie przydziału zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tego zgrupowania, korzystając z tych samych właściwości, z wyjątkiem identyfikatora zasobu, oraz oblicza liczbę rekordów w każdej z tych grup, która jest zwracana w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="0ae24-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="0ae24-169">Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.</span><span class="sxs-lookup"><span data-stu-id="0ae24-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="0ae24-170">Spowoduje to wygenerowanie pierwszych 5 zasad odmowy, które mają najwięcej odmówionych zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ae24-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="0ae24-171">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ae24-171">PARAMETERS</span></span>

### <span data-ttu-id="0ae24-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="0ae24-172">-Apply</span></span>
<span data-ttu-id="0ae24-173">Stosowanie wyrażenia agregacji przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="0ae24-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="0ae24-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae24-174">-DefaultProfile</span></span>
<span data-ttu-id="0ae24-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ae24-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ae24-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="0ae24-176">-Filter</span></span>
<span data-ttu-id="0ae24-177">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="0ae24-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="0ae24-178">-Od</span><span class="sxs-lookup"><span data-stu-id="0ae24-178">-From</span></span>
<span data-ttu-id="0ae24-179">ISO 8601 sformatowana sygnatura czasowa określająca czas rozpoczęcia interwału do kwerendy.</span><span class="sxs-lookup"><span data-stu-id="0ae24-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="0ae24-180">Jeśli nie określono tej wartości, domyślnie przyjmowana jest wartość parametru "to" pomniejszona o 1 dzień.</span><span class="sxs-lookup"><span data-stu-id="0ae24-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae24-181">-ManagementGroupName</span></span>
<span data-ttu-id="0ae24-182">Nazwa grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="0ae24-182">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="0ae24-183">-OrderBy</span></span>
<span data-ttu-id="0ae24-184">Wyrażenie porządkowania przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="0ae24-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="0ae24-185">Jedna lub więcej nazw kolumn rozdzielanych przecinkami z opcjonalną wartością DESC (domyślnie) lub "ASC".</span><span class="sxs-lookup"><span data-stu-id="0ae24-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="0ae24-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0ae24-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="0ae24-187">Nazwa zadania w zasadach.</span><span class="sxs-lookup"><span data-stu-id="0ae24-187">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0ae24-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="0ae24-189">Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="0ae24-189">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0ae24-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="0ae24-191">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="0ae24-191">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae24-192">-ResourceGroupName</span></span>
<span data-ttu-id="0ae24-193">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ae24-193">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ae24-194">-ResourceId</span></span>
<span data-ttu-id="0ae24-195">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0ae24-195">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-196">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="0ae24-196">-Select</span></span>
<span data-ttu-id="0ae24-197">Wybierz wyrażenie przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="0ae24-197">Select expression using OData notation.</span></span>
<span data-ttu-id="0ae24-198">Jedna lub więcej nazw kolumn rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="0ae24-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="0ae24-199">Ogranicza liczbę kolumn w każdym rekordzie do żądanych wartości.</span><span class="sxs-lookup"><span data-stu-id="0ae24-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="0ae24-200">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0ae24-200">-SubscriptionId</span></span>
<span data-ttu-id="0ae24-201">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="0ae24-201">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-202">-To</span><span class="sxs-lookup"><span data-stu-id="0ae24-202">-To</span></span>
<span data-ttu-id="0ae24-203">ISO 8601 sformatowana sygnatura czasowa określająca czas zakończenia interwału do kwerendy.</span><span class="sxs-lookup"><span data-stu-id="0ae24-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="0ae24-204">Jeśli nie określono tego parametru, domyślną wartością jest czas żądania.</span><span class="sxs-lookup"><span data-stu-id="0ae24-204">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-205">-Początek</span><span class="sxs-lookup"><span data-stu-id="0ae24-205">-Top</span></span>
<span data-ttu-id="0ae24-206">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="0ae24-206">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ae24-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae24-207">CommonParameters</span></span>
<span data-ttu-id="0ae24-208">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ae24-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae24-209">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ae24-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae24-210">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ae24-210">INPUTS</span></span>

### <span data-ttu-id="0ae24-211">System. String</span><span class="sxs-lookup"><span data-stu-id="0ae24-211">System.String</span></span>

## <span data-ttu-id="0ae24-212">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ae24-212">OUTPUTS</span></span>

### <span data-ttu-id="0ae24-213">Microsoft. Azure. Commands. PolicyInsights. models. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="0ae24-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="0ae24-214">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ae24-214">NOTES</span></span>

## <span data-ttu-id="0ae24-215">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ae24-215">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193186"
---
# <span data-ttu-id="97197-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="97197-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="97197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97197-102">SYNOPSIS</span></span>
<span data-ttu-id="97197-103">Pobiera zdarzenia oceny zasad generowane w przypadku tworzenia lub aktualizowania zasobów.</span><span class="sxs-lookup"><span data-stu-id="97197-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="97197-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97197-104">SYNTAX</span></span>

### <span data-ttu-id="97197-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="97197-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97197-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="97197-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97197-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="97197-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97197-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="97197-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97197-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="97197-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97197-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="97197-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97197-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="97197-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97197-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="97197-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97197-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="97197-113">DESCRIPTION</span></span>
<span data-ttu-id="97197-114">Pobiera zdarzenia oceny zasad generowane w przypadku tworzenia lub aktualizowania zasobów.</span><span class="sxs-lookup"><span data-stu-id="97197-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="97197-115">Zapytania dotyczące rekordów zdarzeń zasad można używać w różnych zakresach w zależności od określonego interwału czasu (domyślne wartością jest ostatni dzień).</span><span class="sxs-lookup"><span data-stu-id="97197-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="97197-116">Wyniki można filtrować, grupować i obliczać agregacje grup.</span><span class="sxs-lookup"><span data-stu-id="97197-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="97197-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97197-117">EXAMPLES</span></span>

### <span data-ttu-id="97197-118">Przykład 1. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="97197-119">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="97197-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="97197-120">Przykład 2. Uzyskiwanie zdarzeń zasad w zakresie określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="97197-121">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="97197-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="97197-122">Przykład 3. Uzyskiwanie zdarzeń zasad w zakresie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="97197-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="97197-123">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="97197-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="97197-124">Przykład 4. Uzyskiwanie zdarzeń zasad w zakresie grupy zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="97197-125">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="97197-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="97197-126">Przykład 5. Uzyskiwanie zdarzeń zasad w zakresie grupy zasobów w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="97197-127">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="97197-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="97197-128">Przykład 6. Uzyskiwanie zdarzeń zasad dla zasobu</span><span class="sxs-lookup"><span data-stu-id="97197-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="97197-129">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="97197-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="97197-130">Przykład 7. Uzyskiwanie zdarzeń zasad dla definicji zestawu zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="97197-131">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w ramach określonej definicji zestawu zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="97197-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="97197-132">Przykład 8. Uzyskiwanie zdarzeń zasad dla definicji zestawu zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="97197-133">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w ramach określonej definicji zestawu zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="97197-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="97197-134">Przykład 9. Uzyskiwanie zdarzeń zasad dla definicji zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="97197-135">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w kontekście bieżącej sesji) w związku z określoną definicją zasad (która istnieje w subskrypcji w kontekście bieżącej sesji).</span><span class="sxs-lookup"><span data-stu-id="97197-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="97197-136">Przykład 10. Uzyskiwanie zdarzeń zasad dla definicji zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="97197-137">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="97197-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="97197-138">Przykład 11. Uzyskiwanie zdarzeń zasad dla przypisania zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="97197-139">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w związku z określonym przypisaniem zasad (który istnieje w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="97197-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="97197-140">Przykład 12. Uzyskiwanie zdarzeń zasad dla przypisania zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="97197-141">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych przez przypisanie określonych zasad (które istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="97197-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="97197-142">Przykład 13. Uzyskiwanie zdarzeń zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="97197-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="97197-143">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w związku z określonym przydziałem zasad (który istnieje w grupie zasobów w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="97197-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="97197-144">Przykład 14. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji przy użyciu opcji zapytania OrderBy, Top i Select</span><span class="sxs-lookup"><span data-stu-id="97197-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="97197-145">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="97197-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="97197-146">Polecenie uporządkuje wyniki według właściwości sygnatury czasowej i nazwy przydziału zasad i przyjmuje tylko 5 z nich wymienionych w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="97197-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="97197-147">Wybiera on również, aby wyświetlić tylko podzbiór kolumn dla każdego rekordu.</span><span class="sxs-lookup"><span data-stu-id="97197-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="97197-148">Przykład 15. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z opcjami zapytania Od i Do</span><span class="sxs-lookup"><span data-stu-id="97197-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="97197-149">Pobiera rekordy zdarzeń zasad generowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="97197-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="97197-150">Przykład 16. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z opcją zapytania filtru</span><span class="sxs-lookup"><span data-stu-id="97197-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="97197-151">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="97197-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="97197-152">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odrzucania lub inspekcji) i lokalizacji zasobów (z wyłączeniem lokalizacji regionu wschodniego).</span><span class="sxs-lookup"><span data-stu-id="97197-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="97197-153">Przykład 17. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z ustawieniem agregacji Zastosuj do liczby wierszy</span><span class="sxs-lookup"><span data-stu-id="97197-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="97197-154">Pobiera liczbę rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="97197-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="97197-155">To polecenie zwraca liczbę rekordów zdarzeń zasad, która jest zwracana wewnątrz właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="97197-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="97197-156">Przykład 18. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z ustawieniem Zastosuj grupowanie z agregacją</span><span class="sxs-lookup"><span data-stu-id="97197-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="97197-157">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="97197-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="97197-158">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko inspekcję i odrzucanie zdarzeń).</span><span class="sxs-lookup"><span data-stu-id="97197-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="97197-159">Grupuje wyniki na podstawie przypisania zasad, definicji zasad, akcji definicji zasad i identyfikatora zasobu, a następnie oblicza liczbę rekordów w każdej grupie, która jest zwracana we właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="97197-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="97197-160">Wyniki są uporządkowane według agregacji licznika w kolejności malejącej i przyjmuje tylko 5 z nich wymienionych w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="97197-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="97197-161">Przykład 19. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z ustawieniem Zastosuj grupowanie bez agregacji</span><span class="sxs-lookup"><span data-stu-id="97197-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="97197-162">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="97197-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="97197-163">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko inspekcję i odrzucanie zdarzeń).</span><span class="sxs-lookup"><span data-stu-id="97197-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="97197-164">Grupuje wyniki na podstawie identyfikatora zasobu. W wyniku tego zostanie wygenerowana lista wszystkich zasobów w ramach subskrypcji, które wygenerują zdarzenie zasad dla co najmniej jednej inspekcji lub odmów zasad.</span><span class="sxs-lookup"><span data-stu-id="97197-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="97197-165">Przykład 20. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z polem Zastosuj określającą wiele grup</span><span class="sxs-lookup"><span data-stu-id="97197-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="97197-166">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="97197-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="97197-167">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko odrzucanie zdarzeń).</span><span class="sxs-lookup"><span data-stu-id="97197-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="97197-168">Najpierw grupuje wyniki na podstawie przydziałów zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tej grupowania o tych samych właściwościach z wyjątkiem identyfikatora zasobu i oblicza liczbę rekordów w każdej z tych grup, która jest zwracana we właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="97197-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="97197-169">Wyniki są uporządkowane według agregacji licznika w kolejności malejącej i przyjmuje tylko 5 z nich wymienionych w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="97197-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="97197-170">W ten sposób jest generowanych 5 najważniejszych zasad odmów z najwięcej odrzuconych zasobów.</span><span class="sxs-lookup"><span data-stu-id="97197-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="97197-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97197-171">PARAMETERS</span></span>

### <span data-ttu-id="97197-172">— Zastosuj</span><span class="sxs-lookup"><span data-stu-id="97197-172">-Apply</span></span>
<span data-ttu-id="97197-173">Zastosuj wyrażenie dla agregacji przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="97197-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="97197-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97197-174">-DefaultProfile</span></span>
<span data-ttu-id="97197-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97197-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97197-176">— Filtr</span><span class="sxs-lookup"><span data-stu-id="97197-176">-Filter</span></span>
<span data-ttu-id="97197-177">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="97197-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="97197-178">— Od</span><span class="sxs-lookup"><span data-stu-id="97197-178">-From</span></span>
<span data-ttu-id="97197-179">Sygnatura czasowa w formacie ISO 8601 określająca czas rozpoczęcia interwału dla zapytania.</span><span class="sxs-lookup"><span data-stu-id="97197-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="97197-180">Jeśli nie zostanie określona, wartość parametru "To" jest domyślnie określana jako minus 1 dzień.</span><span class="sxs-lookup"><span data-stu-id="97197-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="97197-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="97197-181">-ManagementGroupName</span></span>
<span data-ttu-id="97197-182">Nazwa grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="97197-182">Management group name.</span></span>

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

### <span data-ttu-id="97197-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="97197-183">-OrderBy</span></span>
<span data-ttu-id="97197-184">Wyrażenie kolejności przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="97197-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="97197-185">Co najmniej jedna nazwa kolumny rozdzielona przecinkami z opcjonalnym "desc" (ustawieniem domyślnym) lub "asc".</span><span class="sxs-lookup"><span data-stu-id="97197-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="97197-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="97197-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="97197-187">Nazwa przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="97197-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="97197-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="97197-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="97197-189">Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="97197-189">Policy definition name.</span></span>

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

### <span data-ttu-id="97197-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="97197-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="97197-191">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="97197-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="97197-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97197-192">-ResourceGroupName</span></span>
<span data-ttu-id="97197-193">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97197-193">Resource group name.</span></span>

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

### <span data-ttu-id="97197-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97197-194">-ResourceId</span></span>
<span data-ttu-id="97197-195">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="97197-195">Resource ID.</span></span>

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

### <span data-ttu-id="97197-196">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="97197-196">-Select</span></span>
<span data-ttu-id="97197-197">Zaznacz wyrażenie przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="97197-197">Select expression using OData notation.</span></span>
<span data-ttu-id="97197-198">Co najmniej jedna nazwa kolumny rozdzielona przecinkami.</span><span class="sxs-lookup"><span data-stu-id="97197-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="97197-199">Ogranicza kolumny w każdym rekordzie tylko do tych, o które proszono.</span><span class="sxs-lookup"><span data-stu-id="97197-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="97197-200">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97197-200">-SubscriptionId</span></span>
<span data-ttu-id="97197-201">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="97197-201">Subscription ID.</span></span>

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

### <span data-ttu-id="97197-202">— Do</span><span class="sxs-lookup"><span data-stu-id="97197-202">-To</span></span>
<span data-ttu-id="97197-203">Sygnatura czasowa w formacie ISO 8601 określająca czas zakończenia interwału dla zapytania.</span><span class="sxs-lookup"><span data-stu-id="97197-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="97197-204">Jeśli nie zostanie określona, domyślnie jest określana godzina żądania.</span><span class="sxs-lookup"><span data-stu-id="97197-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="97197-205">— Na górze</span><span class="sxs-lookup"><span data-stu-id="97197-205">-Top</span></span>
<span data-ttu-id="97197-206">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="97197-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="97197-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97197-207">CommonParameters</span></span>
<span data-ttu-id="97197-208">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97197-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97197-209">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97197-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97197-210">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97197-210">INPUTS</span></span>

### <span data-ttu-id="97197-211">System.String</span><span class="sxs-lookup"><span data-stu-id="97197-211">System.String</span></span>

## <span data-ttu-id="97197-212">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97197-212">OUTPUTS</span></span>

### <span data-ttu-id="97197-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="97197-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="97197-214">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97197-214">NOTES</span></span>

## <span data-ttu-id="97197-215">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97197-215">RELATED LINKS</span></span>

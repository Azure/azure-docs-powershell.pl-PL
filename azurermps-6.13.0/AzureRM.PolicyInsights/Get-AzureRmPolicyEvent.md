---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
ms.openlocfilehash: 0c4e4f531dac3f75f0eff69ba1dcfc644473ea06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547359"
---
# <span data-ttu-id="389b2-101">Get-AzureRmPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="389b2-101">Get-AzureRmPolicyEvent</span></span>

## <span data-ttu-id="389b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="389b2-102">SYNOPSIS</span></span>
<span data-ttu-id="389b2-103">Pobiera zdarzenia obliczania zasad generowane po utworzeniu lub zaktualizowaniu zasobów.</span><span class="sxs-lookup"><span data-stu-id="389b2-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="389b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="389b2-104">SYNTAX</span></span>

### <span data-ttu-id="389b2-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="389b2-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="389b2-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="389b2-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="389b2-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="389b2-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="389b2-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="389b2-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="389b2-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="389b2-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="389b2-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="389b2-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="389b2-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="389b2-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="389b2-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="389b2-112">ResourceScope</span></span>
```
Get-AzureRmPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="389b2-113">Opis</span><span class="sxs-lookup"><span data-stu-id="389b2-113">DESCRIPTION</span></span>
<span data-ttu-id="389b2-114">Pobiera zdarzenia obliczania zasad generowane po utworzeniu lub zaktualizowaniu zasobów.</span><span class="sxs-lookup"><span data-stu-id="389b2-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="389b2-115">Rekordy zdarzeń zasad mogą być badane w różnych zakresach na podstawie określonego interwału czasu (domyślnie do ostatniego dnia).</span><span class="sxs-lookup"><span data-stu-id="389b2-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="389b2-116">Wyniki mogą być filtrowane, grupowane, a agregacje grup mogą być obliczane.</span><span class="sxs-lookup"><span data-stu-id="389b2-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="389b2-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="389b2-117">EXAMPLES</span></span>

### <span data-ttu-id="389b2-118">Przykład 1: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent
```

<span data-ttu-id="389b2-119">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="389b2-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="389b2-120">Przykład 2: pobieranie zdarzeń dotyczących zasad w określonym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="389b2-121">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="389b2-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="389b2-122">Przykład 3: pobieranie zdarzeń dotyczących zasad w zakresie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="389b2-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="389b2-123">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="389b2-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="389b2-124">Przykład 4: pobieranie zdarzeń dotyczących zasad w zakresie grupy zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="389b2-125">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="389b2-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="389b2-126">Przykład 5: pobieranie zdarzeń zasad w zakresie grupy zasobów w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="389b2-127">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="389b2-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="389b2-128">Przykład 6: pobieranie zdarzeń dotyczących zasad dla zasobu</span><span class="sxs-lookup"><span data-stu-id="389b2-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="389b2-129">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="389b2-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="389b2-130">Przykład 7: pobieranie zdarzeń dotyczących zasad dla definicji zestawu zasad w bieżącym abonamentzie</span><span class="sxs-lookup"><span data-stu-id="389b2-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="389b2-131">Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (istniejącej w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="389b2-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="389b2-132">Przykład 8: pobieranie zdarzeń dotyczących zasad dla definicji zestawu zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="389b2-133">Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (istniejącej w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="389b2-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="389b2-134">Przykład 9: pobieranie zdarzeń dotyczących zasad dla definicji zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="389b2-135">Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) zgodnie z określoną definicją zasad (istniejącą w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="389b2-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="389b2-136">Przykład 10: pobieranie zdarzeń zasad dla definicji zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="389b2-137">Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) zgodnie z określoną definicją zasad (istniejącą w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="389b2-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="389b2-138">Przykład 11: pobieranie zdarzeń dotyczących zasad dla przypisania zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="389b2-139">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) wykonywane przez określone przypisanie zasad (istniejące w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="389b2-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="389b2-140">Przykład 12: pobieranie zdarzeń zasad dla przydziału zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="389b2-141">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) dokonywanych przez określone przypisanie zasad (istniejące w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="389b2-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="389b2-142">Przykład 13: pobieranie zdarzeń zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="389b2-143">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych przez określone przypisanie zasad (istniejące w grupie zasobów w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="389b2-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="389b2-144">Przykład 14: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji OrderBy, początek i wybierz zapytanie</span><span class="sxs-lookup"><span data-stu-id="389b2-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="389b2-145">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="389b2-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="389b2-146">Polecenie porządkuje wyniki według sygnatury czasowej i właściwości nazw przydziałów, a następnie pobiera tylko 5 najważniejszych osób z listy w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="389b2-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="389b2-147">Wybiera także listę tylko podzestawu kolumn dla każdego rekordu.</span><span class="sxs-lookup"><span data-stu-id="389b2-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="389b2-148">Przykład 15: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji od i do zapytania</span><span class="sxs-lookup"><span data-stu-id="389b2-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="389b2-149">Pobiera rekordy zdarzeń zasad wygenerowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="389b2-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="389b2-150">Przykład 16: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji Filtruj zapytanie</span><span class="sxs-lookup"><span data-stu-id="389b2-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="389b2-151">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="389b2-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="389b2-152">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (dotyczy to odmowy lub akcji inspekcji) oraz lokalizacji zasobów (z pominięciem lokalizacji wschodniego).</span><span class="sxs-lookup"><span data-stu-id="389b2-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="389b2-153">Przykład 17: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu Zastosuj Określanie agregacji liczby wierszy</span><span class="sxs-lookup"><span data-stu-id="389b2-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="389b2-154">Pobiera liczbę rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="389b2-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="389b2-155">Polecenie zwraca liczbę tylko rekordów zdarzeń zasad, które są zwracane w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="389b2-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="389b2-156">Przykład 18: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu Zastosuj Określanie grupowania z agregacją</span><span class="sxs-lookup"><span data-stu-id="389b2-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="389b2-157">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="389b2-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="389b2-158">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko zdarzenia inspekcji i Odmów).</span><span class="sxs-lookup"><span data-stu-id="389b2-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="389b2-159">Umożliwia grupowanie wyników na podstawie przydziału zasad, definicji zasad, akcji definicji zasad i identyfikatora zasobu oraz obliczanie liczby rekordów w każdej grupie, która jest zwracana w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="389b2-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="389b2-160">Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.</span><span class="sxs-lookup"><span data-stu-id="389b2-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="389b2-161">Przykład 19: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie grupowania bez agregacji</span><span class="sxs-lookup"><span data-stu-id="389b2-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="389b2-162">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="389b2-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="389b2-163">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko zdarzenia inspekcji i Odmów).</span><span class="sxs-lookup"><span data-stu-id="389b2-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="389b2-164">Umożliwia grupowanie wyników na podstawie identyfikatora zasobu. Spowoduje to wygenerowanie listy wszystkich zasobów w ramach subskrypcji, które wygenerowały zdarzenie zasad dla co najmniej jednej inspekcji lub zasady odmowy.</span><span class="sxs-lookup"><span data-stu-id="389b2-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="389b2-165">Przykład 20: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie wielu grup</span><span class="sxs-lookup"><span data-stu-id="389b2-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="389b2-166">Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="389b2-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="389b2-167">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (dotyczy tylko zdarzeń Odmów).</span><span class="sxs-lookup"><span data-stu-id="389b2-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="389b2-168">Najpierw grupuje wyniki na podstawie przydziału zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tego zgrupowania, korzystając z tych samych właściwości, z wyjątkiem identyfikatora zasobu, oraz oblicza liczbę rekordów w każdej z tych grup, która jest zwracana w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="389b2-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="389b2-169">Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.</span><span class="sxs-lookup"><span data-stu-id="389b2-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="389b2-170">Spowoduje to wygenerowanie pierwszych 5 zasad odmowy, które mają najwięcej odmówionych zasobów.</span><span class="sxs-lookup"><span data-stu-id="389b2-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="389b2-171">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="389b2-171">PARAMETERS</span></span>

### <span data-ttu-id="389b2-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="389b2-172">-Apply</span></span>
<span data-ttu-id="389b2-173">Stosowanie wyrażenia agregacji przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="389b2-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="389b2-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389b2-174">-DefaultProfile</span></span>
<span data-ttu-id="389b2-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="389b2-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389b2-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="389b2-176">-Filter</span></span>
<span data-ttu-id="389b2-177">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="389b2-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="389b2-178">-Od</span><span class="sxs-lookup"><span data-stu-id="389b2-178">-From</span></span>
<span data-ttu-id="389b2-179">ISO 8601 sformatowana sygnatura czasowa określająca czas rozpoczęcia interwału do kwerendy.</span><span class="sxs-lookup"><span data-stu-id="389b2-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="389b2-180">Jeśli nie określono tej wartości, domyślnie przyjmowana jest wartość parametru "to" pomniejszona o 1 dzień.</span><span class="sxs-lookup"><span data-stu-id="389b2-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="389b2-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="389b2-181">-ManagementGroupName</span></span>
<span data-ttu-id="389b2-182">Nazwa grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="389b2-182">Management group name.</span></span>

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

### <span data-ttu-id="389b2-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="389b2-183">-OrderBy</span></span>
<span data-ttu-id="389b2-184">Wyrażenie porządkowania przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="389b2-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="389b2-185">Jedna lub więcej nazw kolumn rozdzielanych przecinkami z opcjonalną wartością DESC (domyślnie) lub "ASC".</span><span class="sxs-lookup"><span data-stu-id="389b2-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="389b2-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="389b2-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="389b2-187">Nazwa zadania w zasadach.</span><span class="sxs-lookup"><span data-stu-id="389b2-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="389b2-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="389b2-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="389b2-189">Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="389b2-189">Policy definition name.</span></span>

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

### <span data-ttu-id="389b2-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="389b2-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="389b2-191">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="389b2-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="389b2-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="389b2-192">-ResourceGroupName</span></span>
<span data-ttu-id="389b2-193">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="389b2-193">Resource group name.</span></span>

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

### <span data-ttu-id="389b2-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="389b2-194">-ResourceId</span></span>
<span data-ttu-id="389b2-195">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="389b2-195">Resource ID.</span></span>

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

### <span data-ttu-id="389b2-196">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="389b2-196">-Select</span></span>
<span data-ttu-id="389b2-197">Wybierz wyrażenie przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="389b2-197">Select expression using OData notation.</span></span>
<span data-ttu-id="389b2-198">Jedna lub więcej nazw kolumn rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="389b2-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="389b2-199">Ogranicza liczbę kolumn w każdym rekordzie do żądanych wartości.</span><span class="sxs-lookup"><span data-stu-id="389b2-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="389b2-200">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="389b2-200">-SubscriptionId</span></span>
<span data-ttu-id="389b2-201">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="389b2-201">Subscription ID.</span></span>

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

### <span data-ttu-id="389b2-202">-To</span><span class="sxs-lookup"><span data-stu-id="389b2-202">-To</span></span>
<span data-ttu-id="389b2-203">ISO 8601 sformatowana sygnatura czasowa określająca czas zakończenia interwału do kwerendy.</span><span class="sxs-lookup"><span data-stu-id="389b2-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="389b2-204">Jeśli nie określono tego parametru, domyślną wartością jest czas żądania.</span><span class="sxs-lookup"><span data-stu-id="389b2-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="389b2-205">-Początek</span><span class="sxs-lookup"><span data-stu-id="389b2-205">-Top</span></span>
<span data-ttu-id="389b2-206">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="389b2-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="389b2-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389b2-207">CommonParameters</span></span>
<span data-ttu-id="389b2-208">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="389b2-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389b2-209">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="389b2-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389b2-210">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="389b2-210">INPUTS</span></span>

### <span data-ttu-id="389b2-211">System. String</span><span class="sxs-lookup"><span data-stu-id="389b2-211">System.String</span></span>

## <span data-ttu-id="389b2-212">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="389b2-212">OUTPUTS</span></span>

### <span data-ttu-id="389b2-213">Microsoft. Azure. Commands. PolicyInsights. models. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="389b2-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="389b2-214">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="389b2-214">NOTES</span></span>

## <span data-ttu-id="389b2-215">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="389b2-215">RELATED LINKS</span></span>
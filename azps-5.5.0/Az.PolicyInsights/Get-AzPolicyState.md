---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240339"
---
# <span data-ttu-id="da5f7-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="da5f7-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="da5f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="da5f7-103">Pobiera stany zgodności zasad dla zasobów.</span><span class="sxs-lookup"><span data-stu-id="da5f7-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="da5f7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da5f7-104">SYNTAX</span></span>

### <span data-ttu-id="da5f7-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="da5f7-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5f7-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="da5f7-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5f7-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="da5f7-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5f7-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="da5f7-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5f7-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="da5f7-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5f7-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="da5f7-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5f7-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="da5f7-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da5f7-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="da5f7-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da5f7-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="da5f7-113">DESCRIPTION</span></span>
<span data-ttu-id="da5f7-114">Pobiera stany zgodności zasad dla zasobów.</span><span class="sxs-lookup"><span data-stu-id="da5f7-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="da5f7-115">Zapytania dotyczące rekordów stanu zasad można używać w różnych zakresach.</span><span class="sxs-lookup"><span data-stu-id="da5f7-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="da5f7-116">W zależności od określonego interwału czasu (domyślnie do ostatniego dnia) można utworzyć zapytanie dotyczące najnowszych stanów zasad lub wszystkich przejść stanów zasad.</span><span class="sxs-lookup"><span data-stu-id="da5f7-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="da5f7-117">Wyniki można filtrować, grupować i obliczać agregacje grup.</span><span class="sxs-lookup"><span data-stu-id="da5f7-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="da5f7-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da5f7-118">EXAMPLES</span></span>

### <span data-ttu-id="da5f7-119">Przykład 1. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="da5f7-120">Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="da5f7-121">Przykład 2. Uzyskiwanie najnowszych stanów zasad w zakresie określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="da5f7-122">Pobiera rekordy stanu najnowszych zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="da5f7-123">Przykład 3. Uzyskiwanie wszystkich stanów zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="da5f7-124">Pobiera wszystkie historyczne rekordy stanu zasad (w tym najnowsze) wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="da5f7-125">Przykład 4. Uzyskiwanie najnowszych stanów zasad w zakresie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="da5f7-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="da5f7-126">Pobiera najnowsze rekordy stanu zasad generowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="da5f7-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="da5f7-127">Przykład 5. Uzyskiwanie najnowszych stanów zasad w zakresie grupy zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="da5f7-128">Pobiera rekordy stanu najnowszych zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej grupy zasobów (w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="da5f7-129">Przykład 6. Uzyskiwanie najnowszych stanów zasad w zakresie grupy zasobów w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="da5f7-130">Pobiera rekordy stanu najnowszych zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="da5f7-131">Przykład 7. Uzyskiwanie najnowszych stanów zasad dla zasobu</span><span class="sxs-lookup"><span data-stu-id="da5f7-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="da5f7-132">Pobiera rekordy stanu najnowszych zasad wygenerowane w ostatnim dniu dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="da5f7-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="da5f7-133">Przykład 8. Uzyskiwanie najnowszych stanów zasad dla definicji zestawu zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="da5f7-134">Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych definicji zestawu zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="da5f7-135">Przykład 9. Uzyskiwanie najnowszych stanów zasad dla definicji zestawu zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="da5f7-136">Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych na podstawie definicji zestawu określonych zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="da5f7-137">Przykład 10. Uzyskiwanie najnowszych stanów zasad dla definicji zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="da5f7-138">Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w ramach określonej definicji zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="da5f7-139">Przykład 11. Uzyskiwanie najnowszych stanów zasad dla definicji zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="da5f7-140">Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w ramach określonej definicji zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="da5f7-141">Przykład 12. Uzyskiwanie najnowszych stanów zasad dla przypisania zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="da5f7-142">Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych przez przypisanie określonych zasad (które istnieje w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="da5f7-143">Przykład 13. Uzyskiwanie najnowszych stanów zasad dla przypisania zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="da5f7-144">Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych przez przypisanie określonych zasad (które istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="da5f7-145">Przykład 14. Uzyskiwanie najnowszych stanów zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da5f7-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="da5f7-146">Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w związku z określonym przydziałem zasad (który istnieje w grupie zasobów w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="da5f7-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="da5f7-147">Przykład 15. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji za pomocą opcji zapytania OrderBy, Top i Select</span><span class="sxs-lookup"><span data-stu-id="da5f7-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="da5f7-148">Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="da5f7-149">Polecenie uporządkuje wyniki według właściwości sygnatury czasowej i nazwy przydziału zasad i przyjmuje tylko 5 z nich wymienionych w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="da5f7-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="da5f7-150">Wybiera on również, aby wyświetlić tylko podzbiór kolumn dla każdego rekordu.</span><span class="sxs-lookup"><span data-stu-id="da5f7-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="da5f7-151">Przykład 16. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z opcjami zapytania Od i Do</span><span class="sxs-lookup"><span data-stu-id="da5f7-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="da5f7-152">Pobiera najnowsze rekordy stanu zasad generowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="da5f7-153">Przykład 17. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z opcją zapytania filtru</span><span class="sxs-lookup"><span data-stu-id="da5f7-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="da5f7-154">Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="da5f7-155">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odrzucania lub inspekcji), stanu zgodności (obejmuje tylko stan niezgodny) i lokalizacji zasobów (z wyłączeniem lokalizacji regionu wschodniego).</span><span class="sxs-lookup"><span data-stu-id="da5f7-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="da5f7-156">Przykład 18. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z ustawieniem Zastosuj określającą agregację liczby wierszy</span><span class="sxs-lookup"><span data-stu-id="da5f7-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="da5f7-157">Pobiera liczbę rekordów stanu najnowszych zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="da5f7-158">To polecenie zwraca liczbę tylko rekordów stanu zasad, zwracanych wewnątrz właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="da5f7-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="da5f7-159">Przykład 19. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z zastosowaniem określania grupowania z agregacją</span><span class="sxs-lookup"><span data-stu-id="da5f7-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="da5f7-160">Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="da5f7-161">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (obejmuje tylko stan niezgodności).</span><span class="sxs-lookup"><span data-stu-id="da5f7-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="da5f7-162">Grupuje wyniki na podstawie przypisania zasad, definicji zestawu zasad i definicji zasad, a następnie oblicza liczbę rekordów w każdej grupie, która jest zwracana wewnątrz właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="da5f7-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="da5f7-163">Wyniki są uporządkowane według agregacji licznika w kolejności malejącej i przyjmuje tylko 5 z nich wymienionych w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="da5f7-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="da5f7-164">Przykład 20. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z ustawieniem Zastosuj grupowanie bez agregacji</span><span class="sxs-lookup"><span data-stu-id="da5f7-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="da5f7-165">Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="da5f7-166">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (obejmuje tylko stan niezgodności).</span><span class="sxs-lookup"><span data-stu-id="da5f7-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="da5f7-167">Grupuje wyniki na podstawie identyfikatora zasobu. W ten sposób zostanie wygenerowana lista wszystkich zasobów w ramach subskrypcji, które są niezgodne z co najmniej jedną zasadą.</span><span class="sxs-lookup"><span data-stu-id="da5f7-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="da5f7-168">Przykład 21. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z polem Zastosuj określającą wiele grupowania</span><span class="sxs-lookup"><span data-stu-id="da5f7-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="da5f7-169">Przykład 22. Uzyskiwanie najnowszych stanów zasad wraz ze szczegółami oceny zasad dla zasobu</span><span class="sxs-lookup"><span data-stu-id="da5f7-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="da5f7-170">Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="da5f7-171">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (obejmuje tylko stan niezgodności).</span><span class="sxs-lookup"><span data-stu-id="da5f7-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="da5f7-172">Najpierw grupuje wyniki na podstawie przypisania zasad, definicji zestawu zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tej grupowania o tych samych właściwościach z wyjątkiem identyfikatora zasobu i oblicza liczbę rekordów w każdej z tych grup, która jest zwracana we właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="da5f7-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="da5f7-173">Wyniki są uporządkowane według agregacji licznika w kolejności malejącej i przyjmuje tylko 5 z nich wymienionych w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="da5f7-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="da5f7-174">W ten sposób jest generowanych 5 najważniejszych zasad z najwięcej niezgodnych zasobów.</span><span class="sxs-lookup"><span data-stu-id="da5f7-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="da5f7-175">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da5f7-175">PARAMETERS</span></span>

### <span data-ttu-id="da5f7-176">— Wszystko</span><span class="sxs-lookup"><span data-stu-id="da5f7-176">-All</span></span>
<span data-ttu-id="da5f7-177">W określonym interwale czasu pobierz wszystkie stany zasad, a nie tylko najnowsze.</span><span class="sxs-lookup"><span data-stu-id="da5f7-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="da5f7-178">— Zastosuj</span><span class="sxs-lookup"><span data-stu-id="da5f7-178">-Apply</span></span>
<span data-ttu-id="da5f7-179">Zastosuj wyrażenie dla agregacji przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="da5f7-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="da5f7-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5f7-180">-DefaultProfile</span></span>
<span data-ttu-id="da5f7-181">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="da5f7-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da5f7-182">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="da5f7-182">-Expand</span></span>
<span data-ttu-id="da5f7-183">Rozwijanie wyrażenia przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="da5f7-183">Expand expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da5f7-184">— Filtr</span><span class="sxs-lookup"><span data-stu-id="da5f7-184">-Filter</span></span>
<span data-ttu-id="da5f7-185">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="da5f7-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="da5f7-186">— Od</span><span class="sxs-lookup"><span data-stu-id="da5f7-186">-From</span></span>
<span data-ttu-id="da5f7-187">Sygnatura czasowa w formacie ISO 8601 określająca czas rozpoczęcia interwału dla zapytania.</span><span class="sxs-lookup"><span data-stu-id="da5f7-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="da5f7-188">Jeśli nie jest określona, wartość parametru "To" jest domyślnie określana jako minus 1 dzień.</span><span class="sxs-lookup"><span data-stu-id="da5f7-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="da5f7-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="da5f7-189">-ManagementGroupName</span></span>
<span data-ttu-id="da5f7-190">Nazwa grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="da5f7-190">Management group name.</span></span>

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

### <span data-ttu-id="da5f7-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="da5f7-191">-OrderBy</span></span>
<span data-ttu-id="da5f7-192">Wyrażenie kolejności przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="da5f7-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="da5f7-193">Co najmniej jedna nazwa kolumny rozdzielona przecinkami z opcjonalnym "desc" (ustawieniem domyślnym) lub "asc".</span><span class="sxs-lookup"><span data-stu-id="da5f7-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="da5f7-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="da5f7-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="da5f7-195">Nazwa przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="da5f7-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="da5f7-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="da5f7-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="da5f7-197">Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="da5f7-197">Policy definition name.</span></span>

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

### <span data-ttu-id="da5f7-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="da5f7-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="da5f7-199">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="da5f7-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="da5f7-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da5f7-200">-ResourceGroupName</span></span>
<span data-ttu-id="da5f7-201">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="da5f7-201">Resource group name.</span></span>

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

### <span data-ttu-id="da5f7-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da5f7-202">-ResourceId</span></span>
<span data-ttu-id="da5f7-203">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="da5f7-203">Resource ID.</span></span>

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

### <span data-ttu-id="da5f7-204">— Wybierz</span><span class="sxs-lookup"><span data-stu-id="da5f7-204">-Select</span></span>
<span data-ttu-id="da5f7-205">Zaznacz wyrażenie przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="da5f7-205">Select expression using OData notation.</span></span>
<span data-ttu-id="da5f7-206">Co najmniej jedna nazwa kolumny rozdzielona przecinkami.</span><span class="sxs-lookup"><span data-stu-id="da5f7-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="da5f7-207">Ogranicza kolumny w każdym rekordzie tylko do tych, o które proszono.</span><span class="sxs-lookup"><span data-stu-id="da5f7-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="da5f7-208">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da5f7-208">-SubscriptionId</span></span>
<span data-ttu-id="da5f7-209">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da5f7-209">Subscription ID.</span></span>

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

### <span data-ttu-id="da5f7-210">— Do</span><span class="sxs-lookup"><span data-stu-id="da5f7-210">-To</span></span>
<span data-ttu-id="da5f7-211">Sygnatura czasowa w formacie ISO 8601 określająca czas zakończenia interwału dla zapytania.</span><span class="sxs-lookup"><span data-stu-id="da5f7-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="da5f7-212">Jeśli nie zostanie określona, domyślnie jest określana godzina żądania.</span><span class="sxs-lookup"><span data-stu-id="da5f7-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="da5f7-213">— Na górze</span><span class="sxs-lookup"><span data-stu-id="da5f7-213">-Top</span></span>
<span data-ttu-id="da5f7-214">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="da5f7-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="da5f7-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5f7-215">CommonParameters</span></span>
<span data-ttu-id="da5f7-216">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da5f7-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5f7-217">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da5f7-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5f7-218">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da5f7-218">INPUTS</span></span>

### <span data-ttu-id="da5f7-219">System.String</span><span class="sxs-lookup"><span data-stu-id="da5f7-219">System.String</span></span>

## <span data-ttu-id="da5f7-220">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da5f7-220">OUTPUTS</span></span>

### <span data-ttu-id="da5f7-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="da5f7-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="da5f7-222">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da5f7-222">NOTES</span></span>

## <span data-ttu-id="da5f7-223">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da5f7-223">RELATED LINKS</span></span>

[<span data-ttu-id="da5f7-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="da5f7-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)

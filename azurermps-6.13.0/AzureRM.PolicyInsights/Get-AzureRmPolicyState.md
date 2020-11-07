---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
ms.openlocfilehash: 6f5f1c341db0c5f57ffb541b9455369c0c6e5ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716773"
---
# <span data-ttu-id="12d71-101">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="12d71-101">Get-AzureRmPolicyState</span></span>

## <span data-ttu-id="12d71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12d71-102">SYNOPSIS</span></span>
<span data-ttu-id="12d71-103">Pobiera Stany zgodności z zasadami dotyczącymi zasobów.</span><span class="sxs-lookup"><span data-stu-id="12d71-103">Gets policy compliance states for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12d71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12d71-104">SYNTAX</span></span>

### <span data-ttu-id="12d71-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12d71-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d71-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="12d71-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d71-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="12d71-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d71-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="12d71-108">ResourceScope</span></span>
```
Get-AzureRmPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d71-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="12d71-109">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d71-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="12d71-110">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d71-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="12d71-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d71-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="12d71-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12d71-113">Opis</span><span class="sxs-lookup"><span data-stu-id="12d71-113">DESCRIPTION</span></span>
<span data-ttu-id="12d71-114">Pobiera Stany zgodności z zasadami dotyczącymi zasobów.</span><span class="sxs-lookup"><span data-stu-id="12d71-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="12d71-115">Rekordy stanu zasad mogą być badane w różnych zakresach.</span><span class="sxs-lookup"><span data-stu-id="12d71-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="12d71-116">W zależności od określonego interwału czasu (domyślnie jest to ostatni dzień) można wykonać zapytanie dotyczące najnowszych Stanów zasad lub wszystkich przejść między Stanami zasad.</span><span class="sxs-lookup"><span data-stu-id="12d71-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="12d71-117">Wyniki mogą być filtrowane, grupowane, a agregacje grup mogą być obliczane.</span><span class="sxs-lookup"><span data-stu-id="12d71-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="12d71-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12d71-118">EXAMPLES</span></span>

### <span data-ttu-id="12d71-119">Przykład 1: pobieranie najnowszych Stanów zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState
```

<span data-ttu-id="12d71-120">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="12d71-121">Przykład 2: Uzyskiwanie najnowszych Stanów zasad w określonym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="12d71-122">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="12d71-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="12d71-123">Przykład 3: uzyskiwanie wszystkich stanów zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -All
```

<span data-ttu-id="12d71-124">Pobiera wszystkie historyczne rekordy stanu zasad (w tym najnowsze) generowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="12d71-125">Przykład 4: pobieranie najnowszych Stanów zasad w zakresie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="12d71-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="12d71-126">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="12d71-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="12d71-127">Przykład 5: pobieranie najnowszych Stanów zasad w zakresie grupy zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="12d71-128">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów należących do określonej grupy zasobów (w subskrypcji w kontekście bieżącej sesji).</span><span class="sxs-lookup"><span data-stu-id="12d71-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="12d71-129">Przykład 6: pobieranie najnowszych Stanów zasad w zakresie grupy zasobów w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="12d71-130">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów należących do określonej grupy zasobów (w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="12d71-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="12d71-131">Przykład 7: Uzyskiwanie najnowszych Stanów zasad dla zasobu</span><span class="sxs-lookup"><span data-stu-id="12d71-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="12d71-132">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="12d71-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="12d71-133">Przykład 8: Uzyskiwanie najnowszych Stanów zasad dla definicji zestawu zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="12d71-134">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (istniejącej w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="12d71-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="12d71-135">Przykład 9: Uzyskiwanie najnowszych Stanów zasad dla definicji zestawu zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="12d71-136">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="12d71-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="12d71-137">Przykład 10: Uzyskiwanie najnowszych Stanów zasad dla definicji zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="12d71-138">Umożliwia pobieranie najnowszych rekordów stanu zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zasad (istniejącej w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="12d71-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="12d71-139">Przykład 11: pobieranie najnowszych Stanów zasad dla definicji zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="12d71-140">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zasad (istniejącej w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="12d71-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="12d71-141">Przykład 12: Uzyskiwanie najnowszych Stanów zasad dla przypisania zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="12d71-142">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przez określone przypisanie zasad (istniejące w subskrypcji bieżącego kontekstu sesji).</span><span class="sxs-lookup"><span data-stu-id="12d71-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="12d71-143">Przykład 13: Uzyskiwanie najnowszych Stanów zasad dla przypisania zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="12d71-144">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przez określone przypisanie zasad (istniejące w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="12d71-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="12d71-145">Przykład 14: Uzyskiwanie najnowszych Stanów zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="12d71-146">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przez określone przypisanie zasad (istniejące w grupie zasobów w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="12d71-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="12d71-147">Przykład 15: Uzyskiwanie najnowszych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu opcji OrderBy, początek i wybierz zapytanie</span><span class="sxs-lookup"><span data-stu-id="12d71-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="12d71-148">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="12d71-149">Polecenie porządkuje wyniki według sygnatury czasowej i właściwości nazw przydziałów, a następnie pobiera tylko 5 najważniejszych osób z listy w tej kolejności.</span><span class="sxs-lookup"><span data-stu-id="12d71-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="12d71-150">Wybiera także listę tylko podzestawu kolumn dla każdego rekordu.</span><span class="sxs-lookup"><span data-stu-id="12d71-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="12d71-151">Przykład 16: pobieranie najnowszych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu opcji od i do zapytania</span><span class="sxs-lookup"><span data-stu-id="12d71-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="12d71-152">Pobiera najnowsze rekordy Stanów zasad wygenerowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="12d71-153">Przykład 17: Uzyskiwanie najnowszych Stanów zasad w bieżącym zakresie subskrypcji za pomocą opcji filtrowania kwerend</span><span class="sxs-lookup"><span data-stu-id="12d71-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="12d71-154">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="12d71-155">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odmowy lub inspekcji), stan zgodności (dotyczy tylko statusu niezgodnego) i lokalizacji zasobów (z pominięciem lokalizacji wschodniego).</span><span class="sxs-lookup"><span data-stu-id="12d71-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="12d71-156">Przykład 18: pobieranie najnowszych Stanów zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie agregacji liczby wierszy</span><span class="sxs-lookup"><span data-stu-id="12d71-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="12d71-157">Pobiera liczbę najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="12d71-158">Polecenie zwraca liczbę tylko rekordów Stanów zasad, która jest zwracana w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="12d71-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="12d71-159">Przykład 19: pobieranie najnowszych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu Zastosuj Określanie grupowania z agregacją</span><span class="sxs-lookup"><span data-stu-id="12d71-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="12d71-160">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="12d71-161">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (dotyczy tylko statusu niezgodnego).</span><span class="sxs-lookup"><span data-stu-id="12d71-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="12d71-162">Umożliwia grupowanie wyników na podstawie przydziałów zasad, definicji zestawu zasad i definicji zasad oraz obliczanie liczby rekordów w każdej grupie, która jest zwracana w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="12d71-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="12d71-163">Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.</span><span class="sxs-lookup"><span data-stu-id="12d71-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="12d71-164">Przykład 20: Uzyskiwanie najnowszych Stanów zasad w bieżącym zakresie subskrypcji z opcją Zastosuj określającą grupowanie bez agregacji</span><span class="sxs-lookup"><span data-stu-id="12d71-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="12d71-165">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="12d71-166">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (dotyczy tylko statusu niezgodnego).</span><span class="sxs-lookup"><span data-stu-id="12d71-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="12d71-167">Umożliwia grupowanie wyników na podstawie identyfikatora zasobu. Spowoduje to wygenerowanie listy wszystkich zasobów w ramach subskrypcji, które nie są zgodne z co najmniej jednej zasady.</span><span class="sxs-lookup"><span data-stu-id="12d71-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="12d71-168">Przykład 21: Uzyskiwanie najnowszych Stanów zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie wielu grup</span><span class="sxs-lookup"><span data-stu-id="12d71-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

<span data-ttu-id="12d71-169">Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="12d71-169">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="12d71-170">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (dotyczy tylko statusu niezgodnego).</span><span class="sxs-lookup"><span data-stu-id="12d71-170">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="12d71-171">Najpierw grupuje wyniki na podstawie przydziału zasad, definicji zestawu zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tego zgrupowania, korzystając z tych samych właściwości, z wyjątkiem identyfikatora zasobu, oraz oblicza liczbę rekordów w każdej z tych grup, która jest zwracana w ramach właściwości AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="12d71-171">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="12d71-172">Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.</span><span class="sxs-lookup"><span data-stu-id="12d71-172">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="12d71-173">Spowoduje to wygenerowanie pierwszych 5 zasad z największą liczbą niezgodnych zasobów.</span><span class="sxs-lookup"><span data-stu-id="12d71-173">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="12d71-174">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12d71-174">PARAMETERS</span></span>

### <span data-ttu-id="12d71-175">-All</span><span class="sxs-lookup"><span data-stu-id="12d71-175">-All</span></span>
<span data-ttu-id="12d71-176">W określonym przedziale czasu Uzyskaj wszystkie Stany zasad zamiast tylko najnowsze.</span><span class="sxs-lookup"><span data-stu-id="12d71-176">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="12d71-177">-Apply</span><span class="sxs-lookup"><span data-stu-id="12d71-177">-Apply</span></span>
<span data-ttu-id="12d71-178">Stosowanie wyrażenia agregacji przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="12d71-178">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="12d71-179">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d71-179">-DefaultProfile</span></span>
<span data-ttu-id="12d71-180">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12d71-180">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12d71-181">-Filter</span><span class="sxs-lookup"><span data-stu-id="12d71-181">-Filter</span></span>
<span data-ttu-id="12d71-182">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="12d71-182">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="12d71-183">-Od</span><span class="sxs-lookup"><span data-stu-id="12d71-183">-From</span></span>
<span data-ttu-id="12d71-184">ISO 8601 sformatowana sygnatura czasowa określająca czas rozpoczęcia interwału do kwerendy.</span><span class="sxs-lookup"><span data-stu-id="12d71-184">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="12d71-185">Jeśli nie określono tej wartości, domyślnie przyjmowana jest wartość parametru "to" pomniejszona o 1 dzień.</span><span class="sxs-lookup"><span data-stu-id="12d71-185">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="12d71-186">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="12d71-186">-ManagementGroupName</span></span>
<span data-ttu-id="12d71-187">Nazwa grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="12d71-187">Management group name.</span></span>

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

### <span data-ttu-id="12d71-188">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="12d71-188">-OrderBy</span></span>
<span data-ttu-id="12d71-189">Wyrażenie porządkowania przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="12d71-189">Ordering expression using OData notation.</span></span>
<span data-ttu-id="12d71-190">Jedna lub więcej nazw kolumn rozdzielanych przecinkami z opcjonalną wartością DESC (domyślnie) lub "ASC".</span><span class="sxs-lookup"><span data-stu-id="12d71-190">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="12d71-191">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="12d71-191">-PolicyAssignmentName</span></span>
<span data-ttu-id="12d71-192">Nazwa zadania w zasadach.</span><span class="sxs-lookup"><span data-stu-id="12d71-192">Policy assignment name.</span></span>

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

### <span data-ttu-id="12d71-193">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="12d71-193">-PolicyDefinitionName</span></span>
<span data-ttu-id="12d71-194">Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="12d71-194">Policy definition name.</span></span>

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

### <span data-ttu-id="12d71-195">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="12d71-195">-PolicySetDefinitionName</span></span>
<span data-ttu-id="12d71-196">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="12d71-196">Policy set definition name.</span></span>

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

### <span data-ttu-id="12d71-197">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d71-197">-ResourceGroupName</span></span>
<span data-ttu-id="12d71-198">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12d71-198">Resource group name.</span></span>

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

### <span data-ttu-id="12d71-199">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12d71-199">-ResourceId</span></span>
<span data-ttu-id="12d71-200">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="12d71-200">Resource ID.</span></span>

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

### <span data-ttu-id="12d71-201">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="12d71-201">-Select</span></span>
<span data-ttu-id="12d71-202">Wybierz wyrażenie przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="12d71-202">Select expression using OData notation.</span></span>
<span data-ttu-id="12d71-203">Jedna lub więcej nazw kolumn rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="12d71-203">One or more comma-separated column names.</span></span>
<span data-ttu-id="12d71-204">Ogranicza liczbę kolumn w każdym rekordzie do żądanych wartości.</span><span class="sxs-lookup"><span data-stu-id="12d71-204">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="12d71-205">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="12d71-205">-SubscriptionId</span></span>
<span data-ttu-id="12d71-206">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="12d71-206">Subscription ID.</span></span>

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

### <span data-ttu-id="12d71-207">-To</span><span class="sxs-lookup"><span data-stu-id="12d71-207">-To</span></span>
<span data-ttu-id="12d71-208">ISO 8601 sformatowana sygnatura czasowa określająca czas zakończenia interwału do kwerendy.</span><span class="sxs-lookup"><span data-stu-id="12d71-208">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="12d71-209">Jeśli nie określono tego parametru, domyślną wartością jest czas żądania.</span><span class="sxs-lookup"><span data-stu-id="12d71-209">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="12d71-210">-Początek</span><span class="sxs-lookup"><span data-stu-id="12d71-210">-Top</span></span>
<span data-ttu-id="12d71-211">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="12d71-211">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="12d71-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d71-212">CommonParameters</span></span>
<span data-ttu-id="12d71-213">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d71-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d71-214">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d71-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d71-215">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12d71-215">INPUTS</span></span>

### <span data-ttu-id="12d71-216">System. String</span><span class="sxs-lookup"><span data-stu-id="12d71-216">System.String</span></span>

## <span data-ttu-id="12d71-217">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12d71-217">OUTPUTS</span></span>

### <span data-ttu-id="12d71-218">Microsoft. Azure. Commands. PolicyInsights. models. PolicyState</span><span class="sxs-lookup"><span data-stu-id="12d71-218">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="12d71-219">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12d71-219">NOTES</span></span>

## <span data-ttu-id="12d71-220">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12d71-220">RELATED LINKS</span></span>

[<span data-ttu-id="12d71-221">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="12d71-221">Get-AzureRmPolicyStateSummary</span></span>](./Get-AzureRmPolicyStateSummary.md)

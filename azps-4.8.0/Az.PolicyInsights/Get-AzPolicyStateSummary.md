---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223681"
---
# <span data-ttu-id="e0faf-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="e0faf-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="e0faf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0faf-102">SYNOPSIS</span></span>
<span data-ttu-id="e0faf-103">Pobiera ostatnie podsumowanie stanów zgodności zasad dla zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0faf-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="e0faf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0faf-104">SYNTAX</span></span>

### <span data-ttu-id="e0faf-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e0faf-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0faf-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="e0faf-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0faf-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="e0faf-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0faf-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="e0faf-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0faf-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="e0faf-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0faf-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="e0faf-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0faf-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="e0faf-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0faf-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="e0faf-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0faf-113">Opis</span><span class="sxs-lookup"><span data-stu-id="e0faf-113">DESCRIPTION</span></span>
<span data-ttu-id="e0faf-114">Umożliwia wyświetlenie podsumowania najnowszych numerów Stanów zgodności zasad w różnych zakresach z podziałem na przypisania zasad i definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="e0faf-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="e0faf-115">Obejmuje tylko Stany zasad niezgodne z zasadami.</span><span class="sxs-lookup"><span data-stu-id="e0faf-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="e0faf-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0faf-116">EXAMPLES</span></span>

### <span data-ttu-id="e0faf-117">Przykład 1: pobieranie najnowszych niezgodnych Stanów zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="e0faf-118">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="e0faf-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e0faf-119">Przykład 2: Uzyskiwanie najnowszych niezgodnych Stanów zasad w określonym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="e0faf-120">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0faf-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="e0faf-121">Przykład 3: pobieranie najnowszych niezgodnych Stanów zasad w zakresie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="e0faf-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="e0faf-122">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e0faf-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="e0faf-123">Przykład 4: pobieranie najnowszych niezgodnych Stanów zasad w zakresie grupy zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e0faf-124">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów należących do określonej grupy zasobów (w subskrypcji w kontekście bieżącej sesji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="e0faf-125">Przykład 5: pobieranie najnowszych niezgodnych Stanów zasad w zakresie grupy zasobów w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e0faf-126">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów należących do określonej grupy zasobów (w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="e0faf-127">Przykład 6: uzyskiwanie informacji o najnowszych niezgodnych Stanach zasad dla zasobu</span><span class="sxs-lookup"><span data-stu-id="e0faf-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="e0faf-128">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="e0faf-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="e0faf-129">Przykład 7: Pobierz najnowsze niezgodne Stany zasad Podsumowanie dla definicji zestawu zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e0faf-130">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych za pomocą określonej definicji zestawu zasad (która istnieje w kontekście bieżącej sesji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e0faf-131">Przykład 8: pobieranie najnowszych niezgodnych Stanów zasad dla definicji zestawu zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e0faf-132">Umożliwia wyświetlenie widoku podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e0faf-133">Przykład 9: Pobierz najnowsze niezgodne Stany zasad Podsumowanie dla definicji zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e0faf-134">Umożliwia wyświetlenie widoku podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zasad (istniejącej w ramach subskrypcji w kontekście bieżącej sesji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e0faf-135">Przykład 10: pobieranie najnowszych niezgodnych Stanów zasad dla definicji zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e0faf-136">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przeprowadzonych według określonej definicji zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e0faf-137">Przykład 11: pobieranie najnowszych niezgodnych Stanów zasad dla przypisania zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e0faf-138">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych przez określone przypisanie zasad (istniejące w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e0faf-139">Przykład 12: pobieranie najnowszych niezgodnych Stanów zasad dla przypisania zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e0faf-140">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych przez określone przypisanie zasad (istniejące w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e0faf-141">Przykład 13: pobieranie najnowszych niezgodnych Stanów zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e0faf-142">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przeprowadzonych przez określone przypisanie zasad (istniejące w grupie zasobów w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="e0faf-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="e0faf-143">Przykład 14: pobieranie najnowszych niezgodnych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu opcji pierwszych kwerend</span><span class="sxs-lookup"><span data-stu-id="e0faf-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="e0faf-144">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="e0faf-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e0faf-145">Polecenie porządkuje podsumowania przydziałów w wynikach według liczby niezgodnych zasobów w kolejności malejącej i pobiera tylko 5 najważniejszych podsumowań zadań.</span><span class="sxs-lookup"><span data-stu-id="e0faf-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="e0faf-146">Przykład 15: Uzyskiwanie najnowszych niezgodnych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu opcji od i do zapytania</span><span class="sxs-lookup"><span data-stu-id="e0faf-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="e0faf-147">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="e0faf-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e0faf-148">Przykład 16: pobieranie najnowszych niezgodnych Stanów zasad w bieżącym zakresie subskrypcji za pomocą opcji filtrowania kwerend</span><span class="sxs-lookup"><span data-stu-id="e0faf-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="e0faf-149">Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="e0faf-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="e0faf-150">Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odmowy lub inspekcji) oraz lokalizację zasobów (z pominięciem lokalizacji wschodniego).</span><span class="sxs-lookup"><span data-stu-id="e0faf-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="e0faf-151">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0faf-151">PARAMETERS</span></span>

### <span data-ttu-id="e0faf-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0faf-152">-DefaultProfile</span></span>
<span data-ttu-id="e0faf-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0faf-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0faf-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="e0faf-154">-Filter</span></span>
<span data-ttu-id="e0faf-155">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="e0faf-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="e0faf-156">-Od</span><span class="sxs-lookup"><span data-stu-id="e0faf-156">-From</span></span>
<span data-ttu-id="e0faf-157">ISO 8601 sformatowana sygnatura czasowa określająca czas rozpoczęcia interwału do kwerendy.</span><span class="sxs-lookup"><span data-stu-id="e0faf-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="e0faf-158">Jeśli nie określono tej wartości, domyślnie przyjmowana jest wartość parametru "to" pomniejszona o 1 dzień.</span><span class="sxs-lookup"><span data-stu-id="e0faf-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="e0faf-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e0faf-159">-ManagementGroupName</span></span>
<span data-ttu-id="e0faf-160">Nazwa grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e0faf-160">Management group name.</span></span>

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

### <span data-ttu-id="e0faf-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e0faf-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="e0faf-162">Nazwa zadania w zasadach.</span><span class="sxs-lookup"><span data-stu-id="e0faf-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="e0faf-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e0faf-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="e0faf-164">Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="e0faf-164">Policy definition name.</span></span>

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

### <span data-ttu-id="e0faf-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e0faf-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="e0faf-166">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="e0faf-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="e0faf-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0faf-167">-ResourceGroupName</span></span>
<span data-ttu-id="e0faf-168">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0faf-168">Resource group name.</span></span>

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

### <span data-ttu-id="e0faf-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0faf-169">-ResourceId</span></span>
<span data-ttu-id="e0faf-170">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e0faf-170">Resource ID.</span></span>

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

### <span data-ttu-id="e0faf-171">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0faf-171">-SubscriptionId</span></span>
<span data-ttu-id="e0faf-172">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e0faf-172">Subscription ID.</span></span>

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

### <span data-ttu-id="e0faf-173">-To</span><span class="sxs-lookup"><span data-stu-id="e0faf-173">-To</span></span>
<span data-ttu-id="e0faf-174">ISO 8601 sformatowana sygnatura czasowa określająca czas zakończenia interwału do kwerendy.</span><span class="sxs-lookup"><span data-stu-id="e0faf-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="e0faf-175">Jeśli nie określono tego parametru, domyślną wartością jest czas żądania.</span><span class="sxs-lookup"><span data-stu-id="e0faf-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="e0faf-176">-Początek</span><span class="sxs-lookup"><span data-stu-id="e0faf-176">-Top</span></span>
<span data-ttu-id="e0faf-177">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="e0faf-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="e0faf-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0faf-178">CommonParameters</span></span>
<span data-ttu-id="e0faf-179">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0faf-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0faf-180">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0faf-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0faf-181">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0faf-181">INPUTS</span></span>

### <span data-ttu-id="e0faf-182">System. String</span><span class="sxs-lookup"><span data-stu-id="e0faf-182">System.String</span></span>

## <span data-ttu-id="e0faf-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0faf-183">OUTPUTS</span></span>

### <span data-ttu-id="e0faf-184">Microsoft. Azure. Commands. PolicyInsights. models. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="e0faf-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="e0faf-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0faf-185">NOTES</span></span>

## <span data-ttu-id="e0faf-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0faf-186">RELATED LINKS</span></span>

[<span data-ttu-id="e0faf-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e0faf-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)

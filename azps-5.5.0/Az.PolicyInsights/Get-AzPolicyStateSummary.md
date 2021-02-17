---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240331"
---
# <span data-ttu-id="10ab8-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="10ab8-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="10ab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="10ab8-103">Pobiera podsumowanie najnowszych stanów zgodności zasad dla zasobów.</span><span class="sxs-lookup"><span data-stu-id="10ab8-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="10ab8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10ab8-104">SYNTAX</span></span>

### <span data-ttu-id="10ab8-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="10ab8-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10ab8-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="10ab8-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10ab8-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="10ab8-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10ab8-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="10ab8-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10ab8-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="10ab8-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10ab8-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="10ab8-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10ab8-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="10ab8-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10ab8-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="10ab8-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10ab8-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="10ab8-113">DESCRIPTION</span></span>
<span data-ttu-id="10ab8-114">Wyświetla podsumowanie najnowszych numerów stanu zgodności zasad w różnych zakresach, podzielone na przypisania zasad i definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="10ab8-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="10ab8-115">Obejmuje ono tylko stany niezgodnych zasad.</span><span class="sxs-lookup"><span data-stu-id="10ab8-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="10ab8-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10ab8-116">EXAMPLES</span></span>

### <span data-ttu-id="10ab8-117">Przykład 1. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w bieżącym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="10ab8-118">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="10ab8-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="10ab8-119">Przykład 2. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w określonym zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="10ab8-120">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="10ab8-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="10ab8-121">Przykład 3. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w zakresie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="10ab8-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="10ab8-122">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="10ab8-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="10ab8-123">Przykład 4. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w zakresie grupy zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="10ab8-124">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="10ab8-125">Przykład 5. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w zakresie grupy zasobów w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="10ab8-126">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="10ab8-127">Przykład 6. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla zasobu</span><span class="sxs-lookup"><span data-stu-id="10ab8-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="10ab8-128">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="10ab8-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="10ab8-129">Przykład 7. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla definicji zestawu zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="10ab8-130">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zestawu zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="10ab8-131">Przykład 8. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla definicji zestawu zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="10ab8-132">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zestawu zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="10ab8-133">Przykład 9. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla definicji zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="10ab8-134">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="10ab8-135">Przykład 10. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla definicji zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="10ab8-136">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zasad (która istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="10ab8-137">Przykład 11. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla przypisania zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="10ab8-138">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa przypisanie określonych zasad (które istnieje w subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="10ab8-139">Przykład 12. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla przypisania zasad w określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="10ab8-140">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa przypisanie określonych zasad (istnieje w określonej subskrypcji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="10ab8-141">Przykład 13. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10ab8-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="10ab8-142">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa przypisanie określonych zasad (które istnieje w grupie zasobów w ramach subskrypcji w bieżącym kontekście sesji).</span><span class="sxs-lookup"><span data-stu-id="10ab8-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="10ab8-143">Przykład 14. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w bieżącym zakresie subskrypcji z opcją Zapytanie najlepsze</span><span class="sxs-lookup"><span data-stu-id="10ab8-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="10ab8-144">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="10ab8-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="10ab8-145">Polecenie uporządkuje podsumowania przydziałów zasad w wynikach według niezgodnych liczników zasobów w kolejności malejącej i przyjmuje tylko 5 najwyższych sum tych podsumowań przydziałów zasad.</span><span class="sxs-lookup"><span data-stu-id="10ab8-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="10ab8-146">Przykład 15. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w bieżącym zakresie subskrypcji z opcjami zapytania Od i Do</span><span class="sxs-lookup"><span data-stu-id="10ab8-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="10ab8-147">Pobiera widok podsumowania najnowszych stanów zgodności zasad generowanych w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w kontekście bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="10ab8-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="10ab8-148">Przykład 16. Uzyskiwanie podsumowania najnowszych niezgodnych stanów zasad w bieżącym zakresie subskrypcji z opcją zapytania filtru</span><span class="sxs-lookup"><span data-stu-id="10ab8-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="10ab8-149">Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.</span><span class="sxs-lookup"><span data-stu-id="10ab8-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="10ab8-150">To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odmawiania lub inspekcji) i lokalizację zasobu (z wyłączeniem lokalizacji na wschód).</span><span class="sxs-lookup"><span data-stu-id="10ab8-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="10ab8-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10ab8-151">PARAMETERS</span></span>

### <span data-ttu-id="10ab8-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ab8-152">-DefaultProfile</span></span>
<span data-ttu-id="10ab8-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10ab8-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10ab8-154">— Filtr</span><span class="sxs-lookup"><span data-stu-id="10ab8-154">-Filter</span></span>
<span data-ttu-id="10ab8-155">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="10ab8-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="10ab8-156">— Od</span><span class="sxs-lookup"><span data-stu-id="10ab8-156">-From</span></span>
<span data-ttu-id="10ab8-157">Sygnatura czasowa w formacie ISO 8601 określająca czas rozpoczęcia interwału dla zapytania.</span><span class="sxs-lookup"><span data-stu-id="10ab8-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="10ab8-158">Jeśli nie jest określona, wartość parametru "To" jest domyślnie określana jako minus 1 dzień.</span><span class="sxs-lookup"><span data-stu-id="10ab8-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="10ab8-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="10ab8-159">-ManagementGroupName</span></span>
<span data-ttu-id="10ab8-160">Nazwa grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="10ab8-160">Management group name.</span></span>

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

### <span data-ttu-id="10ab8-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="10ab8-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="10ab8-162">Nazwa przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="10ab8-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="10ab8-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="10ab8-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="10ab8-164">Nazwa definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="10ab8-164">Policy definition name.</span></span>

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

### <span data-ttu-id="10ab8-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="10ab8-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="10ab8-166">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="10ab8-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="10ab8-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ab8-167">-ResourceGroupName</span></span>
<span data-ttu-id="10ab8-168">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10ab8-168">Resource group name.</span></span>

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

### <span data-ttu-id="10ab8-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10ab8-169">-ResourceId</span></span>
<span data-ttu-id="10ab8-170">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="10ab8-170">Resource ID.</span></span>

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

### <span data-ttu-id="10ab8-171">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10ab8-171">-SubscriptionId</span></span>
<span data-ttu-id="10ab8-172">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="10ab8-172">Subscription ID.</span></span>

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

### <span data-ttu-id="10ab8-173">— Do</span><span class="sxs-lookup"><span data-stu-id="10ab8-173">-To</span></span>
<span data-ttu-id="10ab8-174">Sygnatura czasowa w formacie ISO 8601 określająca czas zakończenia interwału dla zapytania.</span><span class="sxs-lookup"><span data-stu-id="10ab8-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="10ab8-175">Jeśli nie zostanie określona, domyślnie jest określana godzina żądania.</span><span class="sxs-lookup"><span data-stu-id="10ab8-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="10ab8-176">— Na górze</span><span class="sxs-lookup"><span data-stu-id="10ab8-176">-Top</span></span>
<span data-ttu-id="10ab8-177">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="10ab8-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="10ab8-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ab8-178">CommonParameters</span></span>
<span data-ttu-id="10ab8-179">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ab8-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ab8-180">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10ab8-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ab8-181">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10ab8-181">INPUTS</span></span>

### <span data-ttu-id="10ab8-182">System.String</span><span class="sxs-lookup"><span data-stu-id="10ab8-182">System.String</span></span>

## <span data-ttu-id="10ab8-183">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10ab8-183">OUTPUTS</span></span>

### <span data-ttu-id="10ab8-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="10ab8-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="10ab8-185">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10ab8-185">NOTES</span></span>

## <span data-ttu-id="10ab8-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10ab8-186">RELATED LINKS</span></span>

[<span data-ttu-id="10ab8-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="10ab8-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)

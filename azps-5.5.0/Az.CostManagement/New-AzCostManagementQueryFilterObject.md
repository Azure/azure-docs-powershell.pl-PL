---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196675"
---
# <span data-ttu-id="2a491-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="2a491-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="2a491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a491-102">SYNOPSIS</span></span>
<span data-ttu-id="2a491-103">Tworzenie obiektu w pamięci dla Filtru zapytań</span><span class="sxs-lookup"><span data-stu-id="2a491-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="2a491-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a491-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="2a491-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a491-105">DESCRIPTION</span></span>
<span data-ttu-id="2a491-106">Tworzenie obiektu w pamięci dla Filtru zapytań</span><span class="sxs-lookup"><span data-stu-id="2a491-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="2a491-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a491-107">EXAMPLES</span></span>

### <span data-ttu-id="2a491-108">Przykład 1. Tworzenie obiektu filtru zapytania do eksportowania zarządzania kosztami</span><span class="sxs-lookup"><span data-stu-id="2a491-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="2a491-109">To polecenie tworzy obiekt filtru zapytania do eksportowania zarządzania kosztami.</span><span class="sxs-lookup"><span data-stu-id="2a491-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="2a491-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a491-110">PARAMETERS</span></span>

### <span data-ttu-id="2a491-111">— I</span><span class="sxs-lookup"><span data-stu-id="2a491-111">-And</span></span>
<span data-ttu-id="2a491-112">Logiczne wyrażenie "ORAZ".</span><span class="sxs-lookup"><span data-stu-id="2a491-112">The logical "AND" expression.</span></span>
<span data-ttu-id="2a491-113">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-113">Must have at least 2 items.</span></span>
<span data-ttu-id="2a491-114">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach ORAZ i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="2a491-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a491-115">— Wymiary</span><span class="sxs-lookup"><span data-stu-id="2a491-115">-Dimensions</span></span>
<span data-ttu-id="2a491-116">Ma wyrażenie porównania wymiarów.</span><span class="sxs-lookup"><span data-stu-id="2a491-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="2a491-117">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach WYMIARY i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="2a491-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a491-118">— Nie</span><span class="sxs-lookup"><span data-stu-id="2a491-118">-Not</span></span>
<span data-ttu-id="2a491-119">Logiczne wyrażenie "NOT".</span><span class="sxs-lookup"><span data-stu-id="2a491-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="2a491-120">Aby skonstruować, zobacz sekcję NOT properties (NOTATKI) i utwórz tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="2a491-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a491-121">— Lub</span><span class="sxs-lookup"><span data-stu-id="2a491-121">-Or</span></span>
<span data-ttu-id="2a491-122">Logiczne wyrażenie "LUB".</span><span class="sxs-lookup"><span data-stu-id="2a491-122">The logical "OR" expression.</span></span>
<span data-ttu-id="2a491-123">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-123">Must have at least 2 items.</span></span>
<span data-ttu-id="2a491-124">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach LUB i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="2a491-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a491-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="2a491-125">-Tag</span></span>
<span data-ttu-id="2a491-126">Zawiera wyrażenie porównania tagu.</span><span class="sxs-lookup"><span data-stu-id="2a491-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="2a491-127">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach tagu i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="2a491-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a491-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a491-128">CommonParameters</span></span>
<span data-ttu-id="2a491-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a491-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a491-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a491-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a491-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a491-131">INPUTS</span></span>

## <span data-ttu-id="2a491-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a491-132">OUTPUTS</span></span>

### <span data-ttu-id="2a491-133">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="2a491-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="2a491-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a491-134">NOTES</span></span>

<span data-ttu-id="2a491-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2a491-135">ALIASES</span></span>

<span data-ttu-id="2a491-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2a491-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a491-137">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2a491-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a491-138">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a491-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a491-139">AND <IQueryFilter[]>: Wyrażenie logiczne "AND".</span><span class="sxs-lookup"><span data-stu-id="2a491-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="2a491-140">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a491-141">`[And <IQueryFilter[]>]`: wyrażenie logiczne "ORAZ".</span><span class="sxs-lookup"><span data-stu-id="2a491-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="2a491-142">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a491-143">`[Dimensions <IQueryComparisonExpression>]`: Ma wyrażenie porównania dla wymiaru</span><span class="sxs-lookup"><span data-stu-id="2a491-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="2a491-144">`Name <String>`: nazwa kolumny, która ma być porównywana.</span><span class="sxs-lookup"><span data-stu-id="2a491-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="2a491-145">`Value <String[]>`: tablica wartości do użycia w celu porównania</span><span class="sxs-lookup"><span data-stu-id="2a491-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="2a491-146">`[Not <IQueryFilter>]`: wyrażenie logiczne "NOT".</span><span class="sxs-lookup"><span data-stu-id="2a491-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="2a491-147">`[Or <IQueryFilter[]>]`: wyrażenie logiczne "LUB".</span><span class="sxs-lookup"><span data-stu-id="2a491-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="2a491-148">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a491-149">`[Tag <IQueryComparisonExpression>]`: zawiera wyrażenie porównania tagu</span><span class="sxs-lookup"><span data-stu-id="2a491-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="2a491-150">WYMIARY: <IQueryComparisonExpression> zawiera wyrażenie porównania wymiarów.</span><span class="sxs-lookup"><span data-stu-id="2a491-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="2a491-151">`Name <String>`: nazwa kolumny, która ma być porównywana.</span><span class="sxs-lookup"><span data-stu-id="2a491-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="2a491-152">`Value <String[]>`: tablica wartości do użycia w celu porównania</span><span class="sxs-lookup"><span data-stu-id="2a491-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="2a491-153">NOT: <IQueryFilter> Wyrażenie logiczne "NOT".</span><span class="sxs-lookup"><span data-stu-id="2a491-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="2a491-154">`[And <IQueryFilter[]>]`: wyrażenie logiczne "ORAZ".</span><span class="sxs-lookup"><span data-stu-id="2a491-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="2a491-155">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a491-156">`[Dimensions <IQueryComparisonExpression>]`: Ma wyrażenie porównania dla wymiaru</span><span class="sxs-lookup"><span data-stu-id="2a491-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="2a491-157">`Name <String>`: nazwa kolumny, która ma być porównywana.</span><span class="sxs-lookup"><span data-stu-id="2a491-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="2a491-158">`Value <String[]>`: tablica wartości do użycia w celu porównania</span><span class="sxs-lookup"><span data-stu-id="2a491-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="2a491-159">`[Not <IQueryFilter>]`: wyrażenie logiczne "NOT".</span><span class="sxs-lookup"><span data-stu-id="2a491-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="2a491-160">`[Or <IQueryFilter[]>]`: wyrażenie logiczne "LUB".</span><span class="sxs-lookup"><span data-stu-id="2a491-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="2a491-161">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a491-162">`[Tag <IQueryComparisonExpression>]`: zawiera wyrażenie porównania tagu</span><span class="sxs-lookup"><span data-stu-id="2a491-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="2a491-163">OR <IQueryFilter[]>: Wyrażenie logiczne "OR".</span><span class="sxs-lookup"><span data-stu-id="2a491-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="2a491-164">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a491-165">`[And <IQueryFilter[]>]`: wyrażenie logiczne "ORAZ".</span><span class="sxs-lookup"><span data-stu-id="2a491-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="2a491-166">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a491-167">`[Dimensions <IQueryComparisonExpression>]`: Ma wyrażenie porównania dla wymiaru</span><span class="sxs-lookup"><span data-stu-id="2a491-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="2a491-168">`Name <String>`: nazwa kolumny, która ma być porównywana.</span><span class="sxs-lookup"><span data-stu-id="2a491-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="2a491-169">`Value <String[]>`: tablica wartości do użycia w celu porównania</span><span class="sxs-lookup"><span data-stu-id="2a491-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="2a491-170">`[Not <IQueryFilter>]`: wyrażenie logiczne "NOT".</span><span class="sxs-lookup"><span data-stu-id="2a491-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="2a491-171">`[Or <IQueryFilter[]>]`: wyrażenie logiczne "LUB".</span><span class="sxs-lookup"><span data-stu-id="2a491-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="2a491-172">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="2a491-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="2a491-173">`[Tag <IQueryComparisonExpression>]`: zawiera wyrażenie porównania tagu</span><span class="sxs-lookup"><span data-stu-id="2a491-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="2a491-174">TAG: <IQueryComparisonExpression> Zawiera wyrażenie porównania tagu.</span><span class="sxs-lookup"><span data-stu-id="2a491-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="2a491-175">`Name <String>`: nazwa kolumny, która ma być porównywana.</span><span class="sxs-lookup"><span data-stu-id="2a491-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="2a491-176">`Value <String[]>`: tablica wartości do użycia w celu porównania</span><span class="sxs-lookup"><span data-stu-id="2a491-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="2a491-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a491-177">RELATED LINKS</span></span>


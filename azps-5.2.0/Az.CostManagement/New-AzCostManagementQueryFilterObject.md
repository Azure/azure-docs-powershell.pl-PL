---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336613"
---
# <span data-ttu-id="73e33-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="73e33-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="73e33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73e33-102">SYNOPSIS</span></span>
<span data-ttu-id="73e33-103">Tworzenie obiektu w pamięci dla QueryFilter</span><span class="sxs-lookup"><span data-stu-id="73e33-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="73e33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73e33-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="73e33-105">Opis</span><span class="sxs-lookup"><span data-stu-id="73e33-105">DESCRIPTION</span></span>
<span data-ttu-id="73e33-106">Tworzenie obiektu w pamięci dla QueryFilter</span><span class="sxs-lookup"><span data-stu-id="73e33-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="73e33-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73e33-107">EXAMPLES</span></span>

### <span data-ttu-id="73e33-108">Przykład 1. Tworzenie obiektu filtru zapytania na potrzeby eksportu zarządzania kosztami</span><span class="sxs-lookup"><span data-stu-id="73e33-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="73e33-109">to polecenie tworzy obiekt Filter zapytania na potrzeby eksportu zarządzania kosztami.</span><span class="sxs-lookup"><span data-stu-id="73e33-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="73e33-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73e33-110">PARAMETERS</span></span>

### <span data-ttu-id="73e33-111">-And</span><span class="sxs-lookup"><span data-stu-id="73e33-111">-And</span></span>
<span data-ttu-id="73e33-112">Wyrażenie logiczne "AND".</span><span class="sxs-lookup"><span data-stu-id="73e33-112">The logical "AND" expression.</span></span>
<span data-ttu-id="73e33-113">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-113">Must have at least 2 items.</span></span>
<span data-ttu-id="73e33-114">Aby skonstruować, zobacz sekcję notatki i właściwości i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="73e33-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="73e33-115">-Dimensions</span><span class="sxs-lookup"><span data-stu-id="73e33-115">-Dimensions</span></span>
<span data-ttu-id="73e33-116">Zawiera wyrażenie porównania wymiarów.</span><span class="sxs-lookup"><span data-stu-id="73e33-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="73e33-117">Aby skonstruować, zobacz sekcję notatki dla właściwości wymiarów i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="73e33-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="73e33-118">-Not</span><span class="sxs-lookup"><span data-stu-id="73e33-118">-Not</span></span>
<span data-ttu-id="73e33-119">Logiczne wyrażenie "NOT".</span><span class="sxs-lookup"><span data-stu-id="73e33-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="73e33-120">Aby skonstruować, zobacz sekcję notatki dla właściwości NOT Properties i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="73e33-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73e33-121">-Or</span><span class="sxs-lookup"><span data-stu-id="73e33-121">-Or</span></span>
<span data-ttu-id="73e33-122">Wyrażenie logiczne "OR".</span><span class="sxs-lookup"><span data-stu-id="73e33-122">The logical "OR" expression.</span></span>
<span data-ttu-id="73e33-123">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-123">Must have at least 2 items.</span></span>
<span data-ttu-id="73e33-124">Aby skonstruować, zobacz sekcję notatek dla lub właściwości i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="73e33-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="73e33-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="73e33-125">-Tag</span></span>
<span data-ttu-id="73e33-126">Zawiera wyrażenie porównania dla znacznika.</span><span class="sxs-lookup"><span data-stu-id="73e33-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="73e33-127">Aby skonstruować, zobacz sekcję notatki dla właściwości ZNACZNIKÓW i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="73e33-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="73e33-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e33-128">CommonParameters</span></span>
<span data-ttu-id="73e33-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73e33-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e33-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73e33-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e33-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73e33-131">INPUTS</span></span>

## <span data-ttu-id="73e33-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73e33-132">OUTPUTS</span></span>

### <span data-ttu-id="73e33-133">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. Api20200601. QueryFilter</span><span class="sxs-lookup"><span data-stu-id="73e33-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="73e33-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73e33-134">NOTES</span></span>

<span data-ttu-id="73e33-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="73e33-135">ALIASES</span></span>

<span data-ttu-id="73e33-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73e33-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73e33-137">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="73e33-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73e33-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73e33-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73e33-139">I <IQueryFilter [] >: wyrażenie logiczne "AND".</span><span class="sxs-lookup"><span data-stu-id="73e33-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="73e33-140">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="73e33-141">`[And <IQueryFilter[]>]`: Wyrażenie logiczne "AND".</span><span class="sxs-lookup"><span data-stu-id="73e33-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="73e33-142">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="73e33-143">`[Dimensions <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla wymiaru</span><span class="sxs-lookup"><span data-stu-id="73e33-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="73e33-144">`Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.</span><span class="sxs-lookup"><span data-stu-id="73e33-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="73e33-145">`Operator <OperatorType>`: Operator używany do porównywania.</span><span class="sxs-lookup"><span data-stu-id="73e33-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="73e33-146">`Value <String[]>`: Tablica wartości do użycia w porównaniu</span><span class="sxs-lookup"><span data-stu-id="73e33-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="73e33-147">`[Not <IQueryFilter>]`: Logiczne wyrażenie "NOT".</span><span class="sxs-lookup"><span data-stu-id="73e33-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="73e33-148">`[Or <IQueryFilter[]>]`: Wyrażenie logiczne "OR".</span><span class="sxs-lookup"><span data-stu-id="73e33-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="73e33-149">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="73e33-150">`[Tag <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla znacznika</span><span class="sxs-lookup"><span data-stu-id="73e33-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="73e33-151">Wymiary <IQueryComparisonExpression> : zawiera wyrażenie porównawcze dla wymiarów.</span><span class="sxs-lookup"><span data-stu-id="73e33-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="73e33-152">`Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.</span><span class="sxs-lookup"><span data-stu-id="73e33-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="73e33-153">`Operator <OperatorType>`: Operator używany do porównywania.</span><span class="sxs-lookup"><span data-stu-id="73e33-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="73e33-154">`Value <String[]>`: Tablica wartości do użycia w porównaniu</span><span class="sxs-lookup"><span data-stu-id="73e33-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="73e33-155">NOT <IQueryFilter> : logiczne wyrażenie "not".</span><span class="sxs-lookup"><span data-stu-id="73e33-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="73e33-156">`[And <IQueryFilter[]>]`: Wyrażenie logiczne "AND".</span><span class="sxs-lookup"><span data-stu-id="73e33-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="73e33-157">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="73e33-158">`[Dimensions <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla wymiaru</span><span class="sxs-lookup"><span data-stu-id="73e33-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="73e33-159">`Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.</span><span class="sxs-lookup"><span data-stu-id="73e33-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="73e33-160">`Operator <OperatorType>`: Operator używany do porównywania.</span><span class="sxs-lookup"><span data-stu-id="73e33-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="73e33-161">`Value <String[]>`: Tablica wartości do użycia w porównaniu</span><span class="sxs-lookup"><span data-stu-id="73e33-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="73e33-162">`[Not <IQueryFilter>]`: Logiczne wyrażenie "NOT".</span><span class="sxs-lookup"><span data-stu-id="73e33-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="73e33-163">`[Or <IQueryFilter[]>]`: Wyrażenie logiczne "OR".</span><span class="sxs-lookup"><span data-stu-id="73e33-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="73e33-164">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="73e33-165">`[Tag <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla znacznika</span><span class="sxs-lookup"><span data-stu-id="73e33-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="73e33-166">LUB <IQueryFilter [] >: wyrażenie logiczne "OR".</span><span class="sxs-lookup"><span data-stu-id="73e33-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="73e33-167">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="73e33-168">`[And <IQueryFilter[]>]`: Wyrażenie logiczne "AND".</span><span class="sxs-lookup"><span data-stu-id="73e33-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="73e33-169">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="73e33-170">`[Dimensions <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla wymiaru</span><span class="sxs-lookup"><span data-stu-id="73e33-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="73e33-171">`Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.</span><span class="sxs-lookup"><span data-stu-id="73e33-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="73e33-172">`Operator <OperatorType>`: Operator używany do porównywania.</span><span class="sxs-lookup"><span data-stu-id="73e33-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="73e33-173">`Value <String[]>`: Tablica wartości do użycia w porównaniu</span><span class="sxs-lookup"><span data-stu-id="73e33-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="73e33-174">`[Not <IQueryFilter>]`: Logiczne wyrażenie "NOT".</span><span class="sxs-lookup"><span data-stu-id="73e33-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="73e33-175">`[Or <IQueryFilter[]>]`: Wyrażenie logiczne "OR".</span><span class="sxs-lookup"><span data-stu-id="73e33-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="73e33-176">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="73e33-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="73e33-177">`[Tag <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla znacznika</span><span class="sxs-lookup"><span data-stu-id="73e33-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="73e33-178">TAG <IQueryComparisonExpression> : zawiera wyrażenie porównania dla znacznika.</span><span class="sxs-lookup"><span data-stu-id="73e33-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="73e33-179">`Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.</span><span class="sxs-lookup"><span data-stu-id="73e33-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="73e33-180">`Operator <OperatorType>`: Operator używany do porównywania.</span><span class="sxs-lookup"><span data-stu-id="73e33-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="73e33-181">`Value <String[]>`: Tablica wartości do użycia w porównaniu</span><span class="sxs-lookup"><span data-stu-id="73e33-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="73e33-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73e33-182">RELATED LINKS</span></span>


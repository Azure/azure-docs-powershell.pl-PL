---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 608736e8ddb85b877995bed8a42b9bd629dcdba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181171"
---
# <span data-ttu-id="09098-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="09098-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="09098-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09098-102">SYNOPSIS</span></span>
<span data-ttu-id="09098-103">Tworzenie obiektu w pamięci dla zapytania QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="09098-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="09098-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09098-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="09098-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="09098-105">DESCRIPTION</span></span>
<span data-ttu-id="09098-106">Tworzenie obiektu w pamięci dla zapytania QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="09098-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="09098-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09098-107">EXAMPLES</span></span>

### <span data-ttu-id="09098-108">Przykład 1. Tworzenie obiektu wyrażenia porównania zapytania do eksportowania zarządzania kosztami</span><span class="sxs-lookup"><span data-stu-id="09098-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="09098-109">To polecenie tworzy obiekt wyrażenia porównania zapytania do eksportowania zarządzania kosztami.</span><span class="sxs-lookup"><span data-stu-id="09098-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="09098-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09098-110">PARAMETERS</span></span>

### <span data-ttu-id="09098-111">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09098-111">-Name</span></span>
<span data-ttu-id="09098-112">Nazwa kolumny, która ma być porównywana.</span><span class="sxs-lookup"><span data-stu-id="09098-112">The name of the column to use in comparison.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09098-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="09098-113">-Operator</span></span>
<span data-ttu-id="09098-114">Operator, który ma być porównywany.</span><span class="sxs-lookup"><span data-stu-id="09098-114">The operator to use for comparison.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09098-115">— Wartość</span><span class="sxs-lookup"><span data-stu-id="09098-115">-Value</span></span>
<span data-ttu-id="09098-116">Tablica wartości do użycia w celu porównania.</span><span class="sxs-lookup"><span data-stu-id="09098-116">Array of values to use for comparison.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09098-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09098-117">CommonParameters</span></span>
<span data-ttu-id="09098-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09098-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09098-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09098-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09098-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09098-120">INPUTS</span></span>

## <span data-ttu-id="09098-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09098-121">OUTPUTS</span></span>

### <span data-ttu-id="09098-122">Microsoft.Azure.PowerShell.cmdlet.costManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="09098-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="09098-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09098-123">NOTES</span></span>

<span data-ttu-id="09098-124">ALIASY</span><span class="sxs-lookup"><span data-stu-id="09098-124">ALIASES</span></span>

## <span data-ttu-id="09098-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09098-125">RELATED LINKS</span></span>


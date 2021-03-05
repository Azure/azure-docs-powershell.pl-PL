---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: b41c5a30a1425778e69fbfff42cfe7062c6b71b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998173"
---
# <span data-ttu-id="f27eb-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="f27eb-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="f27eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f27eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f27eb-103">Tworzenie obiektu w pamięci dla zapytania QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="f27eb-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="f27eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f27eb-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="f27eb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f27eb-105">DESCRIPTION</span></span>
<span data-ttu-id="f27eb-106">Tworzenie obiektu w pamięci dla zapytania QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="f27eb-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="f27eb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f27eb-107">EXAMPLES</span></span>

### <span data-ttu-id="f27eb-108">Przykład 1. Tworzenie obiektu wyrażenia porównania zapytania do eksportowania zarządzania kosztami</span><span class="sxs-lookup"><span data-stu-id="f27eb-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="f27eb-109">To polecenie tworzy obiekt wyrażenia porównania zapytania do eksportowania zarządzania kosztami.</span><span class="sxs-lookup"><span data-stu-id="f27eb-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="f27eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f27eb-110">PARAMETERS</span></span>

### <span data-ttu-id="f27eb-111">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f27eb-111">-Name</span></span>
<span data-ttu-id="f27eb-112">Nazwa kolumny, która ma być porównywana.</span><span class="sxs-lookup"><span data-stu-id="f27eb-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="f27eb-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="f27eb-113">-Operator</span></span>
<span data-ttu-id="f27eb-114">Operator, który ma być porównywany.</span><span class="sxs-lookup"><span data-stu-id="f27eb-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="f27eb-115">— Wartość</span><span class="sxs-lookup"><span data-stu-id="f27eb-115">-Value</span></span>
<span data-ttu-id="f27eb-116">Tablica wartości do użycia w celu porównania.</span><span class="sxs-lookup"><span data-stu-id="f27eb-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="f27eb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27eb-117">CommonParameters</span></span>
<span data-ttu-id="f27eb-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f27eb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27eb-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f27eb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27eb-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f27eb-120">INPUTS</span></span>

## <span data-ttu-id="f27eb-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f27eb-121">OUTPUTS</span></span>

### <span data-ttu-id="f27eb-122">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="f27eb-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="f27eb-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f27eb-123">NOTES</span></span>

<span data-ttu-id="f27eb-124">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f27eb-124">ALIASES</span></span>

## <span data-ttu-id="f27eb-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f27eb-125">RELATED LINKS</span></span>


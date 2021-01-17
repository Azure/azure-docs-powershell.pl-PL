---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336637"
---
# <span data-ttu-id="3356e-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="3356e-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="3356e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3356e-102">SYNOPSIS</span></span>
<span data-ttu-id="3356e-103">Tworzenie obiektu w pamięci dla QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="3356e-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="3356e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3356e-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="3356e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3356e-105">DESCRIPTION</span></span>
<span data-ttu-id="3356e-106">Tworzenie obiektu w pamięci dla QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="3356e-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="3356e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3356e-107">EXAMPLES</span></span>

### <span data-ttu-id="3356e-108">Przykład 1. Tworzenie obiektu wyrażenia porównawczego zapytania na potrzeby eksportu zarządzania kosztami</span><span class="sxs-lookup"><span data-stu-id="3356e-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="3356e-109">To polecenie tworzy obiekt wyrażenia porównania zapytania na potrzeby eksportu zarządzania kosztami.</span><span class="sxs-lookup"><span data-stu-id="3356e-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="3356e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3356e-110">PARAMETERS</span></span>

### <span data-ttu-id="3356e-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3356e-111">-Name</span></span>
<span data-ttu-id="3356e-112">Nazwa kolumny do użycia w porównaniu.</span><span class="sxs-lookup"><span data-stu-id="3356e-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="3356e-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="3356e-113">-Operator</span></span>
<span data-ttu-id="3356e-114">Operator używany do porównywania.</span><span class="sxs-lookup"><span data-stu-id="3356e-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="3356e-115">-Value</span><span class="sxs-lookup"><span data-stu-id="3356e-115">-Value</span></span>
<span data-ttu-id="3356e-116">Tablica wartości, które mają zostać użyte do porównania.</span><span class="sxs-lookup"><span data-stu-id="3356e-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="3356e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3356e-117">CommonParameters</span></span>
<span data-ttu-id="3356e-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3356e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3356e-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3356e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3356e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3356e-120">INPUTS</span></span>

## <span data-ttu-id="3356e-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3356e-121">OUTPUTS</span></span>

### <span data-ttu-id="3356e-122">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. Api20200601. QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="3356e-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="3356e-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3356e-123">NOTES</span></span>

<span data-ttu-id="3356e-124">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3356e-124">ALIASES</span></span>

## <span data-ttu-id="3356e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3356e-125">RELATED LINKS</span></span>


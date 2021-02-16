---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199482"
---
# <span data-ttu-id="858c6-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="858c6-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="858c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858c6-102">SYNOPSIS</span></span>
<span data-ttu-id="858c6-103">Uzyskiwanie listy budżetów w ramach subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="858c6-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="858c6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="858c6-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="858c6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="858c6-105">DESCRIPTION</span></span>
<span data-ttu-id="858c6-106">Polecenie Get-AzConsumptionBudget cmdlet pobiera listę budżetów w ramach subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="858c6-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="858c6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="858c6-107">EXAMPLES</span></span>

### <span data-ttu-id="858c6-108">Przykład 1. Uzyskiwanie listy budżetów na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="858c6-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="858c6-109">Przykład 2. Uzyskiwanie listy budżetów na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="858c6-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="858c6-110">Przykład 3. Uzyskiwanie budżetu z nazwą budżetu na poziomie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="858c6-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="858c6-111">Przykład 4. Uzyskiwanie budżetu z nazwą budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="858c6-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="858c6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="858c6-112">PARAMETERS</span></span>

### <span data-ttu-id="858c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858c6-113">-DefaultProfile</span></span>
<span data-ttu-id="858c6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="858c6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="858c6-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="858c6-115">-Name</span></span>
<span data-ttu-id="858c6-116">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="858c6-116">Name of a budget.</span></span>

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

### <span data-ttu-id="858c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="858c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="858c6-118">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="858c6-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="858c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858c6-119">CommonParameters</span></span>
<span data-ttu-id="858c6-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="858c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858c6-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858c6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858c6-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="858c6-122">INPUTS</span></span>

### <span data-ttu-id="858c6-123">Brak</span><span class="sxs-lookup"><span data-stu-id="858c6-123">None</span></span>

## <span data-ttu-id="858c6-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="858c6-124">OUTPUTS</span></span>

### <span data-ttu-id="858c6-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="858c6-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="858c6-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="858c6-126">NOTES</span></span>

## <span data-ttu-id="858c6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="858c6-127">RELATED LINKS</span></span>

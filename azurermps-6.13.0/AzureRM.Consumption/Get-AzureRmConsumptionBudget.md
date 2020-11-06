---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionBudget.md
ms.openlocfilehash: 7793dfe2f5d83e0975a5a8c200d19b48d8c4d9f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541795"
---
# <span data-ttu-id="3bc97-101">Get-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="3bc97-101">Get-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="3bc97-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bc97-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc97-103">Zapoznaj się z listą budżetów w subskrypcji lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3bc97-103">Get a list of budgets in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bc97-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bc97-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="3bc97-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3bc97-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc97-106">Polecenie cmdlet Get-AzureRmConsumptionBudget pobiera listę budżetów w subskrypcji lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3bc97-106">The Get-AzureRmConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="3bc97-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bc97-107">EXAMPLES</span></span>

### <span data-ttu-id="3bc97-108">Przykład 1: uzyskiwanie listy budżetów na poziomie abonamentu</span><span class="sxs-lookup"><span data-stu-id="3bc97-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget
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

### <span data-ttu-id="3bc97-109">Przykład 2: uzyskiwanie listy budżetów na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3bc97-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -ResourceGroupName RGBudgets
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

### <span data-ttu-id="3bc97-110">Przykład 3: pobieranie budżetu z nazwą budżetu na poziomie abonamentu</span><span class="sxs-lookup"><span data-stu-id="3bc97-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget
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

### <span data-ttu-id="3bc97-111">Przykład 4: pobieranie budżetu z nazwą budżetu na poziomie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3bc97-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
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

## <span data-ttu-id="3bc97-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bc97-112">PARAMETERS</span></span>

### <span data-ttu-id="3bc97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc97-113">-DefaultProfile</span></span>
<span data-ttu-id="3bc97-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc97-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3bc97-115">-Name</span></span>
<span data-ttu-id="3bc97-116">Nazwa budżetu.</span><span class="sxs-lookup"><span data-stu-id="3bc97-116">Name of a budget.</span></span>

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

### <span data-ttu-id="3bc97-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc97-117">-ResourceGroupName</span></span>
<span data-ttu-id="3bc97-118">Grupa zasobów budżetu.</span><span class="sxs-lookup"><span data-stu-id="3bc97-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="3bc97-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc97-119">CommonParameters</span></span>
<span data-ttu-id="3bc97-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc97-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc97-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc97-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc97-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bc97-122">INPUTS</span></span>

### <span data-ttu-id="3bc97-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3bc97-123">None</span></span>

## <span data-ttu-id="3bc97-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bc97-124">OUTPUTS</span></span>

### <span data-ttu-id="3bc97-125">Microsoft. Azure. Commands.. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="3bc97-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="3bc97-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bc97-126">NOTES</span></span>

## <span data-ttu-id="3bc97-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bc97-127">RELATED LINKS</span></span>

---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb583ca37f610d47c880fd2e15ae3e7b8182b5ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522921"
---
# <span data-ttu-id="67a24-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="67a24-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="67a24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67a24-102">SYNOPSIS</span></span>
<span data-ttu-id="67a24-103">Pobierz zbiór wszystkich nabytych planów, do których subskrypcja ma dostęp.</span><span class="sxs-lookup"><span data-stu-id="67a24-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="67a24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67a24-104">SYNTAX</span></span>

### <span data-ttu-id="67a24-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="67a24-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="67a24-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="67a24-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="67a24-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="67a24-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="67a24-108">Opis</span><span class="sxs-lookup"><span data-stu-id="67a24-108">DESCRIPTION</span></span>
<span data-ttu-id="67a24-109">Pobierz zbiór wszystkich nabytych planów, do których subskrypcja ma dostęp.</span><span class="sxs-lookup"><span data-stu-id="67a24-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="67a24-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67a24-110">EXAMPLES</span></span>

### <span data-ttu-id="67a24-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="67a24-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="67a24-112">Pobierz zbiór wszystkich nabytych planów, do których subskrypcja ma dostęp.</span><span class="sxs-lookup"><span data-stu-id="67a24-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="67a24-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67a24-113">PARAMETERS</span></span>

### <span data-ttu-id="67a24-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="67a24-114">-AcquisitionId</span></span>
<span data-ttu-id="67a24-115">Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="67a24-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a24-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67a24-116">-ResourceId</span></span>
<span data-ttu-id="67a24-117">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="67a24-117">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a24-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="67a24-118">-Skip</span></span>
<span data-ttu-id="67a24-119">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="67a24-119">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a24-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67a24-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="67a24-121">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="67a24-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a24-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="67a24-122">-Top</span></span>
<span data-ttu-id="67a24-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="67a24-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="67a24-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="67a24-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a24-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a24-125">CommonParameters</span></span>
<span data-ttu-id="67a24-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a24-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a24-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a24-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a24-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67a24-128">INPUTS</span></span>

## <span data-ttu-id="67a24-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67a24-129">OUTPUTS</span></span>

### <span data-ttu-id="67a24-130">Microsoft. AzureStack. Management. Subscriptions. admin. models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="67a24-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="67a24-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67a24-131">NOTES</span></span>

## <span data-ttu-id="67a24-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67a24-132">RELATED LINKS</span></span>

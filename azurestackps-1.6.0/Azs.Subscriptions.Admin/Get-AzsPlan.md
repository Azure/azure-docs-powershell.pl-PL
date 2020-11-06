---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523754"
---
# <span data-ttu-id="7f6c2-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="7f6c2-101">Get-AzsPlan</span></span>

## <span data-ttu-id="7f6c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6c2-103">Lista wszystkich planów we wszystkich abonamentach.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="7f6c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f6c2-104">SYNTAX</span></span>

### <span data-ttu-id="7f6c2-105">ListAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f6c2-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7f6c2-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7f6c2-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="7f6c2-107">Lista</span><span class="sxs-lookup"><span data-stu-id="7f6c2-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7f6c2-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="7f6c2-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7f6c2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7f6c2-109">DESCRIPTION</span></span>
<span data-ttu-id="7f6c2-110">Lista wszystkich planów we wszystkich abonamentach.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="7f6c2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f6c2-111">EXAMPLES</span></span>

### <span data-ttu-id="7f6c2-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f6c2-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="7f6c2-113">Pobierz plan konkretną w ramach tych abonamentów.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="7f6c2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f6c2-114">PARAMETERS</span></span>

### <span data-ttu-id="7f6c2-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f6c2-115">-Name</span></span>
<span data-ttu-id="7f6c2-116">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-116">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f6c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f6c2-118">Nazwa grupy zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f6c2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f6c2-119">-ResourceId</span></span>
<span data-ttu-id="7f6c2-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-120">The resource id.</span></span>

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

### <span data-ttu-id="7f6c2-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="7f6c2-121">-Skip</span></span>
<span data-ttu-id="7f6c2-122">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f6c2-123">-Początek</span><span class="sxs-lookup"><span data-stu-id="7f6c2-123">-Top</span></span>
<span data-ttu-id="7f6c2-124">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7f6c2-125">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f6c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6c2-126">CommonParameters</span></span>
<span data-ttu-id="7f6c2-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6c2-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6c2-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f6c2-129">INPUTS</span></span>

## <span data-ttu-id="7f6c2-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f6c2-130">OUTPUTS</span></span>

### <span data-ttu-id="7f6c2-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. plan</span><span class="sxs-lookup"><span data-stu-id="7f6c2-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="7f6c2-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f6c2-132">NOTES</span></span>

## <span data-ttu-id="7f6c2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f6c2-133">RELATED LINKS</span></span>


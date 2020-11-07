---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888902"
---
# <span data-ttu-id="401c8-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="401c8-101">Get-AzsPlan</span></span>

## <span data-ttu-id="401c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="401c8-102">SYNOPSIS</span></span>
<span data-ttu-id="401c8-103">Lista wszystkich planów we wszystkich abonamentach.</span><span class="sxs-lookup"><span data-stu-id="401c8-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="401c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="401c8-104">SYNTAX</span></span>

### <span data-ttu-id="401c8-105">ListAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="401c8-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="401c8-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="401c8-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="401c8-107">Lista</span><span class="sxs-lookup"><span data-stu-id="401c8-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="401c8-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="401c8-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="401c8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="401c8-109">DESCRIPTION</span></span>
<span data-ttu-id="401c8-110">Lista wszystkich planów we wszystkich abonamentach.</span><span class="sxs-lookup"><span data-stu-id="401c8-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="401c8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="401c8-111">EXAMPLES</span></span>

### <span data-ttu-id="401c8-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="401c8-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="401c8-113">Pobierz plan konkretną w ramach tych abonamentów.</span><span class="sxs-lookup"><span data-stu-id="401c8-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="401c8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="401c8-114">PARAMETERS</span></span>

### <span data-ttu-id="401c8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="401c8-115">-Name</span></span>
<span data-ttu-id="401c8-116">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="401c8-116">Name of the plan.</span></span>

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

### <span data-ttu-id="401c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="401c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="401c8-118">Nazwa grupy zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="401c8-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="401c8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="401c8-119">-ResourceId</span></span>
<span data-ttu-id="401c8-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="401c8-120">The resource id.</span></span>

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

### <span data-ttu-id="401c8-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="401c8-121">-Skip</span></span>
<span data-ttu-id="401c8-122">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="401c8-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="401c8-123">-Początek</span><span class="sxs-lookup"><span data-stu-id="401c8-123">-Top</span></span>
<span data-ttu-id="401c8-124">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="401c8-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="401c8-125">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="401c8-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="401c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401c8-126">CommonParameters</span></span>
<span data-ttu-id="401c8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="401c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401c8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="401c8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401c8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="401c8-129">INPUTS</span></span>

## <span data-ttu-id="401c8-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="401c8-130">OUTPUTS</span></span>

### <span data-ttu-id="401c8-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. plan</span><span class="sxs-lookup"><span data-stu-id="401c8-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="401c8-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="401c8-132">NOTES</span></span>

## <span data-ttu-id="401c8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="401c8-133">RELATED LINKS</span></span>


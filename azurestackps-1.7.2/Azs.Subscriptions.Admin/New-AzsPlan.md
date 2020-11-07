---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cddc7e5b3e0d9c7181248e024982293d1418e680
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888398"
---
# <span data-ttu-id="3bd84-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="3bd84-101">New-AzsPlan</span></span>

## <span data-ttu-id="3bd84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bd84-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd84-103">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="3bd84-103">Creates a new plan</span></span>

## <span data-ttu-id="3bd84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bd84-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd84-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3bd84-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd84-106">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="3bd84-106">Creates a new plan</span></span>

## <span data-ttu-id="3bd84-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bd84-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd84-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3bd84-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="3bd84-109">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="3bd84-109">Creates a new plan</span></span>

## <span data-ttu-id="3bd84-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bd84-110">PARAMETERS</span></span>

### <span data-ttu-id="3bd84-111">— Opis</span><span class="sxs-lookup"><span data-stu-id="3bd84-111">-Description</span></span>
<span data-ttu-id="3bd84-112">Opis planu.</span><span class="sxs-lookup"><span data-stu-id="3bd84-112">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3bd84-113">-DisplayName</span></span>
<span data-ttu-id="3bd84-114">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="3bd84-114">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="3bd84-115">-ExternalReferenceId</span></span>
<span data-ttu-id="3bd84-116">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="3bd84-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3bd84-117">-Location</span></span>
<span data-ttu-id="3bd84-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3bd84-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3bd84-119">-Name</span></span>
<span data-ttu-id="3bd84-120">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="3bd84-120">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="3bd84-121">-QuotaIds</span></span>
<span data-ttu-id="3bd84-122">Identyfikatory przydziałów w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="3bd84-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd84-123">-ResourceGroupName</span></span>
<span data-ttu-id="3bd84-124">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="3bd84-124">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="3bd84-125">-SkuIds</span></span>
<span data-ttu-id="3bd84-126">Identyfikatory wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="3bd84-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="3bd84-127">-SubscriptionCount</span></span>
<span data-ttu-id="3bd84-128">Liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="3bd84-128">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bd84-129">-Confirm</span></span>
<span data-ttu-id="3bd84-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bd84-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd84-131">-WhatIf</span></span>
<span data-ttu-id="3bd84-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bd84-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd84-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bd84-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd84-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd84-134">CommonParameters</span></span>
<span data-ttu-id="3bd84-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd84-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd84-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd84-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd84-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bd84-137">INPUTS</span></span>

## <span data-ttu-id="3bd84-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bd84-138">OUTPUTS</span></span>

### <span data-ttu-id="3bd84-139">Microsoft. AzureStack. Management. Subscriptions. admin. models. plan</span><span class="sxs-lookup"><span data-stu-id="3bd84-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="3bd84-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bd84-140">NOTES</span></span>

## <span data-ttu-id="3bd84-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bd84-141">RELATED LINKS</span></span>


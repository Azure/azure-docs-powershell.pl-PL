---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889994"
---
# <span data-ttu-id="48e92-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="48e92-101">New-AzsPlan</span></span>

## <span data-ttu-id="48e92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48e92-102">SYNOPSIS</span></span>
<span data-ttu-id="48e92-103">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="48e92-103">Creates a new plan</span></span>

## <span data-ttu-id="48e92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48e92-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48e92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48e92-105">DESCRIPTION</span></span>
<span data-ttu-id="48e92-106">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="48e92-106">Creates a new plan</span></span>

## <span data-ttu-id="48e92-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48e92-107">EXAMPLES</span></span>

### <span data-ttu-id="48e92-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="48e92-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="48e92-109">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="48e92-109">Creates a new plan</span></span>

## <span data-ttu-id="48e92-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48e92-110">PARAMETERS</span></span>

### <span data-ttu-id="48e92-111">— Opis</span><span class="sxs-lookup"><span data-stu-id="48e92-111">-Description</span></span>
<span data-ttu-id="48e92-112">Opis planu.</span><span class="sxs-lookup"><span data-stu-id="48e92-112">Description of the plan.</span></span>

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

### <span data-ttu-id="48e92-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="48e92-113">-DisplayName</span></span>
<span data-ttu-id="48e92-114">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="48e92-114">Display name.</span></span>

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

### <span data-ttu-id="48e92-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="48e92-115">-ExternalReferenceId</span></span>
<span data-ttu-id="48e92-116">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="48e92-116">External reference identifier.</span></span>

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

### <span data-ttu-id="48e92-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="48e92-117">-Location</span></span>
<span data-ttu-id="48e92-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="48e92-118">Location of the resource.</span></span>

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

### <span data-ttu-id="48e92-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48e92-119">-Name</span></span>
<span data-ttu-id="48e92-120">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="48e92-120">Name of the plan.</span></span>

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

### <span data-ttu-id="48e92-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="48e92-121">-QuotaIds</span></span>
<span data-ttu-id="48e92-122">Identyfikatory przydziałów w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="48e92-122">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="48e92-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e92-123">-ResourceGroupName</span></span>
<span data-ttu-id="48e92-124">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="48e92-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="48e92-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="48e92-125">-SkuIds</span></span>
<span data-ttu-id="48e92-126">Identyfikatory wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="48e92-126">SKU identifiers.</span></span>

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

### <span data-ttu-id="48e92-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="48e92-127">-SubscriptionCount</span></span>
<span data-ttu-id="48e92-128">Liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="48e92-128">Subscription count.</span></span>

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

### <span data-ttu-id="48e92-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48e92-129">-Confirm</span></span>
<span data-ttu-id="48e92-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48e92-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48e92-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48e92-131">-WhatIf</span></span>
<span data-ttu-id="48e92-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48e92-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48e92-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48e92-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48e92-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e92-134">CommonParameters</span></span>
<span data-ttu-id="48e92-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48e92-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e92-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e92-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e92-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48e92-137">INPUTS</span></span>

## <span data-ttu-id="48e92-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48e92-138">OUTPUTS</span></span>

### <span data-ttu-id="48e92-139">Microsoft. AzureStack. Management. Subscriptions. admin. models. plan</span><span class="sxs-lookup"><span data-stu-id="48e92-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="48e92-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48e92-140">NOTES</span></span>

## <span data-ttu-id="48e92-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48e92-141">RELATED LINKS</span></span>


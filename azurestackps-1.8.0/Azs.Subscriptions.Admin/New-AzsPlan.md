---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888897"
---
# <span data-ttu-id="36ba6-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="36ba6-101">New-AzsPlan</span></span>

## <span data-ttu-id="36ba6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="36ba6-103">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="36ba6-103">Creates a new plan</span></span>

## <span data-ttu-id="36ba6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36ba6-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ba6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36ba6-105">DESCRIPTION</span></span>
<span data-ttu-id="36ba6-106">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="36ba6-106">Creates a new plan</span></span>

## <span data-ttu-id="36ba6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36ba6-107">EXAMPLES</span></span>

### <span data-ttu-id="36ba6-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="36ba6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="36ba6-109">Tworzy nowy plan</span><span class="sxs-lookup"><span data-stu-id="36ba6-109">Creates a new plan</span></span>

## <span data-ttu-id="36ba6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36ba6-110">PARAMETERS</span></span>

### <span data-ttu-id="36ba6-111">— Opis</span><span class="sxs-lookup"><span data-stu-id="36ba6-111">-Description</span></span>
<span data-ttu-id="36ba6-112">Opis planu.</span><span class="sxs-lookup"><span data-stu-id="36ba6-112">Description of the plan.</span></span>

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

### <span data-ttu-id="36ba6-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="36ba6-113">-DisplayName</span></span>
<span data-ttu-id="36ba6-114">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="36ba6-114">Display name.</span></span>

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

### <span data-ttu-id="36ba6-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="36ba6-115">-ExternalReferenceId</span></span>
<span data-ttu-id="36ba6-116">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="36ba6-116">External reference identifier.</span></span>

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

### <span data-ttu-id="36ba6-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="36ba6-117">-Location</span></span>
<span data-ttu-id="36ba6-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="36ba6-118">Location of the resource.</span></span>

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

### <span data-ttu-id="36ba6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36ba6-119">-Name</span></span>
<span data-ttu-id="36ba6-120">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="36ba6-120">Name of the plan.</span></span>

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

### <span data-ttu-id="36ba6-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="36ba6-121">-QuotaIds</span></span>
<span data-ttu-id="36ba6-122">Identyfikatory przydziałów w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="36ba6-122">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="36ba6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ba6-123">-ResourceGroupName</span></span>
<span data-ttu-id="36ba6-124">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="36ba6-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="36ba6-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="36ba6-125">-SkuIds</span></span>
<span data-ttu-id="36ba6-126">Identyfikatory wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="36ba6-126">SKU identifiers.</span></span>

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

### <span data-ttu-id="36ba6-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="36ba6-127">-SubscriptionCount</span></span>
<span data-ttu-id="36ba6-128">Liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="36ba6-128">Subscription count.</span></span>

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

### <span data-ttu-id="36ba6-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36ba6-129">-Confirm</span></span>
<span data-ttu-id="36ba6-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ba6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ba6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ba6-131">-WhatIf</span></span>
<span data-ttu-id="36ba6-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ba6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ba6-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36ba6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ba6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ba6-134">CommonParameters</span></span>
<span data-ttu-id="36ba6-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ba6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ba6-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ba6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ba6-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36ba6-137">INPUTS</span></span>

## <span data-ttu-id="36ba6-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36ba6-138">OUTPUTS</span></span>

### <span data-ttu-id="36ba6-139">Microsoft. AzureStack. Management. Subscriptions. admin. models. plan</span><span class="sxs-lookup"><span data-stu-id="36ba6-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="36ba6-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36ba6-140">NOTES</span></span>

## <span data-ttu-id="36ba6-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36ba6-141">RELATED LINKS</span></span>


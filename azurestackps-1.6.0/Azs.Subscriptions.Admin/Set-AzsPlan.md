---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f03365a81fc53af14e3fc9e686504ef3e4387c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523442"
---
# <span data-ttu-id="1745e-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="1745e-101">Set-AzsPlan</span></span>

## <span data-ttu-id="1745e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1745e-102">SYNOPSIS</span></span>
<span data-ttu-id="1745e-103">Umożliwia zaktualizowanie określonego planu</span><span class="sxs-lookup"><span data-stu-id="1745e-103">Updates the specified plan</span></span>

## <span data-ttu-id="1745e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1745e-104">SYNTAX</span></span>

### <span data-ttu-id="1745e-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1745e-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1745e-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="1745e-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1745e-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1745e-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1745e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1745e-108">DESCRIPTION</span></span>
<span data-ttu-id="1745e-109">Umożliwia zaktualizowanie określonego planu</span><span class="sxs-lookup"><span data-stu-id="1745e-109">Updates the specified plan</span></span>

## <span data-ttu-id="1745e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1745e-110">EXAMPLES</span></span>

### <span data-ttu-id="1745e-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1745e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="1745e-112">Umożliwia zaktualizowanie określonego planu</span><span class="sxs-lookup"><span data-stu-id="1745e-112">Updates the specified plan</span></span>

## <span data-ttu-id="1745e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1745e-113">PARAMETERS</span></span>

### <span data-ttu-id="1745e-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="1745e-114">-Description</span></span>
<span data-ttu-id="1745e-115">Opis planu.</span><span class="sxs-lookup"><span data-stu-id="1745e-115">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1745e-116">-DisplayName</span></span>
<span data-ttu-id="1745e-117">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="1745e-117">Display name.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="1745e-118">-ExternalReferenceId</span></span>
<span data-ttu-id="1745e-119">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="1745e-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1745e-120">-InputObject</span></span>
<span data-ttu-id="1745e-121">Obiekt wejściowy typu Microsoft. AzureStack. Management. Subscriptions. admin. modele. plan.</span><span class="sxs-lookup"><span data-stu-id="1745e-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1745e-122">-Location</span></span>
<span data-ttu-id="1745e-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1745e-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1745e-124">-Name</span></span>
<span data-ttu-id="1745e-125">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="1745e-125">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="1745e-126">-QuotaIds</span></span>
<span data-ttu-id="1745e-127">Identyfikatory przydziałów w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="1745e-127">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1745e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1745e-129">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="1745e-129">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1745e-130">-ResourceId</span></span>
<span data-ttu-id="1745e-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1745e-131">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="1745e-132">-SkuIds</span></span>
<span data-ttu-id="1745e-133">Identyfikatory wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="1745e-133">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="1745e-134">-SubscriptionCount</span></span>
<span data-ttu-id="1745e-135">Liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="1745e-135">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1745e-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1745e-136">-Confirm</span></span>
<span data-ttu-id="1745e-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1745e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1745e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1745e-138">-WhatIf</span></span>
<span data-ttu-id="1745e-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1745e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1745e-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1745e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1745e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1745e-141">CommonParameters</span></span>
<span data-ttu-id="1745e-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1745e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1745e-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1745e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1745e-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1745e-144">INPUTS</span></span>

## <span data-ttu-id="1745e-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1745e-145">OUTPUTS</span></span>

### <span data-ttu-id="1745e-146">Microsoft. AzureStack. Management. Subscriptions. admin. models. plan</span><span class="sxs-lookup"><span data-stu-id="1745e-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="1745e-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1745e-147">NOTES</span></span>

## <span data-ttu-id="1745e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1745e-148">RELATED LINKS</span></span>

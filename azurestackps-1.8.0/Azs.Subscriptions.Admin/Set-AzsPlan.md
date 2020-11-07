---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889189"
---
# <span data-ttu-id="68a35-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="68a35-101">Set-AzsPlan</span></span>

## <span data-ttu-id="68a35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68a35-102">SYNOPSIS</span></span>
<span data-ttu-id="68a35-103">Umożliwia zaktualizowanie określonego planu</span><span class="sxs-lookup"><span data-stu-id="68a35-103">Updates the specified plan</span></span>

## <span data-ttu-id="68a35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68a35-104">SYNTAX</span></span>

### <span data-ttu-id="68a35-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="68a35-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68a35-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="68a35-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68a35-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="68a35-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68a35-108">Opis</span><span class="sxs-lookup"><span data-stu-id="68a35-108">DESCRIPTION</span></span>
<span data-ttu-id="68a35-109">Umożliwia zaktualizowanie określonego planu</span><span class="sxs-lookup"><span data-stu-id="68a35-109">Updates the specified plan</span></span>

## <span data-ttu-id="68a35-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68a35-110">EXAMPLES</span></span>

### <span data-ttu-id="68a35-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="68a35-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="68a35-112">Umożliwia zaktualizowanie określonego planu</span><span class="sxs-lookup"><span data-stu-id="68a35-112">Updates the specified plan</span></span>

## <span data-ttu-id="68a35-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68a35-113">PARAMETERS</span></span>

### <span data-ttu-id="68a35-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="68a35-114">-Description</span></span>
<span data-ttu-id="68a35-115">Opis planu.</span><span class="sxs-lookup"><span data-stu-id="68a35-115">Description of the plan.</span></span>

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

### <span data-ttu-id="68a35-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="68a35-116">-DisplayName</span></span>
<span data-ttu-id="68a35-117">Nazwa wyświetlana.</span><span class="sxs-lookup"><span data-stu-id="68a35-117">Display name.</span></span>

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

### <span data-ttu-id="68a35-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="68a35-118">-ExternalReferenceId</span></span>
<span data-ttu-id="68a35-119">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="68a35-119">External reference identifier.</span></span>

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

### <span data-ttu-id="68a35-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68a35-120">-InputObject</span></span>
<span data-ttu-id="68a35-121">Obiekt wejściowy typu Microsoft. AzureStack. Management. Subscriptions. admin. modele. plan.</span><span class="sxs-lookup"><span data-stu-id="68a35-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

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

### <span data-ttu-id="68a35-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="68a35-122">-Location</span></span>
<span data-ttu-id="68a35-123">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="68a35-123">Location of the resource.</span></span>

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

### <span data-ttu-id="68a35-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68a35-124">-Name</span></span>
<span data-ttu-id="68a35-125">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="68a35-125">Name of the plan.</span></span>

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

### <span data-ttu-id="68a35-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="68a35-126">-QuotaIds</span></span>
<span data-ttu-id="68a35-127">Identyfikatory przydziałów w ramach planu.</span><span class="sxs-lookup"><span data-stu-id="68a35-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="68a35-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a35-128">-ResourceGroupName</span></span>
<span data-ttu-id="68a35-129">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="68a35-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="68a35-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68a35-130">-ResourceId</span></span>
<span data-ttu-id="68a35-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="68a35-131">The resource id.</span></span>

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

### <span data-ttu-id="68a35-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="68a35-132">-SkuIds</span></span>
<span data-ttu-id="68a35-133">Identyfikatory wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="68a35-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="68a35-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="68a35-134">-SubscriptionCount</span></span>
<span data-ttu-id="68a35-135">Liczba abonamentów.</span><span class="sxs-lookup"><span data-stu-id="68a35-135">Subscription count.</span></span>

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

### <span data-ttu-id="68a35-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68a35-136">-Confirm</span></span>
<span data-ttu-id="68a35-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68a35-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a35-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a35-138">-WhatIf</span></span>
<span data-ttu-id="68a35-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68a35-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68a35-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68a35-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a35-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a35-141">CommonParameters</span></span>
<span data-ttu-id="68a35-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a35-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a35-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a35-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a35-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68a35-144">INPUTS</span></span>

## <span data-ttu-id="68a35-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68a35-145">OUTPUTS</span></span>

### <span data-ttu-id="68a35-146">Microsoft. AzureStack. Management. Subscriptions. admin. models. plan</span><span class="sxs-lookup"><span data-stu-id="68a35-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="68a35-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68a35-147">NOTES</span></span>

## <span data-ttu-id="68a35-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68a35-148">RELATED LINKS</span></span>


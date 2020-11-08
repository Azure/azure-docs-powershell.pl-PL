---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224880"
---
# <span data-ttu-id="a49fb-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="a49fb-101">New-AzReservation</span></span>

## <span data-ttu-id="a49fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a49fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a49fb-103">Kupowanie rezerwacji</span><span class="sxs-lookup"><span data-stu-id="a49fb-103">Purchase a reservation</span></span>

## <span data-ttu-id="a49fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a49fb-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a49fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a49fb-105">DESCRIPTION</span></span>
<span data-ttu-id="a49fb-106">Zakup wystąpienia rezerwacji i uzyskiwanie korzyści</span><span class="sxs-lookup"><span data-stu-id="a49fb-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="a49fb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a49fb-107">EXAMPLES</span></span>

### <span data-ttu-id="a49fb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a49fb-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="a49fb-109">Po obliczeniu ceny klient może Purcahse, że RI zapewnia calculatePrice</span><span class="sxs-lookup"><span data-stu-id="a49fb-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="a49fb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a49fb-110">PARAMETERS</span></span>

### <span data-ttu-id="a49fb-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="a49fb-111">-AppliedScope</span></span>
<span data-ttu-id="a49fb-112">Abonament, na który zostaną zastosowane świadczenia.</span><span class="sxs-lookup"><span data-stu-id="a49fb-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="a49fb-113">Wymagane, jeśli--zastosowano-Scope-Type (jeden).</span><span class="sxs-lookup"><span data-stu-id="a49fb-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="a49fb-114">Nie określaj, czy--zastosowano-zakres-typ jest udostępniony.</span><span class="sxs-lookup"><span data-stu-id="a49fb-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="a49fb-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="a49fb-115">-AppliedScopeType</span></span>
<span data-ttu-id="a49fb-116">Typ zastosowanego zakresu w celu zaktualizowania rezerwacji za pomocą "jednego" lub "udostępnionego"</span><span class="sxs-lookup"><span data-stu-id="a49fb-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="a49fb-117">-BillingPlan</span></span>
<span data-ttu-id="a49fb-118">Opcje planu rozliczeń dostępne dla tej jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="a49fb-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="a49fb-119">"Co miesiąc" lub "z przodu"</span><span class="sxs-lookup"><span data-stu-id="a49fb-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="a49fb-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="a49fb-120">-BillingScopeId</span></span>
<span data-ttu-id="a49fb-121">Abonament naliczany na potrzeby rezerwacji zakupów.</span><span class="sxs-lookup"><span data-stu-id="a49fb-121">Subscription that will be charged for purchasing Reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a49fb-122">-DefaultProfile</span></span>
<span data-ttu-id="a49fb-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a49fb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a49fb-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a49fb-124">-DisplayName</span></span>
<span data-ttu-id="a49fb-125">Przyjazna nazwa użytkownika w celu łatwego identyfikowania rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="a49fb-125">Friendly name for user to easily identified the reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="a49fb-126">-InstanceFlexibility</span></span>
<span data-ttu-id="a49fb-127">{{Fill InstanceFlexibility Description}}</span><span class="sxs-lookup"><span data-stu-id="a49fb-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="a49fb-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a49fb-128">-Location</span></span>
<span data-ttu-id="a49fb-129">Lokalizacja, w której dostępna jest jednostka SKU.</span><span class="sxs-lookup"><span data-stu-id="a49fb-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="a49fb-130">-Ilość</span><span class="sxs-lookup"><span data-stu-id="a49fb-130">-Quantity</span></span>
<span data-ttu-id="a49fb-131">Ilość produktu do obliczania ceny lub zakupu.</span><span class="sxs-lookup"><span data-stu-id="a49fb-131">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-132">-Renew</span><span class="sxs-lookup"><span data-stu-id="a49fb-132">-Renew</span></span>
<span data-ttu-id="a49fb-133">Ustawienie wartości true spowoduje automatyczne zakupienie nowej rezerwacji w dniu daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="a49fb-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a49fb-134">-ReservationOrderId</span></span>
<span data-ttu-id="a49fb-135">Identyfikator zamówienia rezerwacji do zakupu, wygenerowane przez AZ rezerwacji — Obliczanie zamówienia.</span><span class="sxs-lookup"><span data-stu-id="a49fb-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="a49fb-136">-ReservedResourceType</span></span>
<span data-ttu-id="a49fb-137">Typ zasobu, dla którego należy podać jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="a49fb-137">Type of the resource for which the skus should be provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="a49fb-138">-Sku</span></span>
<span data-ttu-id="a49fb-139">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="a49fb-139">Sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-140">-Term</span><span class="sxs-lookup"><span data-stu-id="a49fb-140">-Term</span></span>
<span data-ttu-id="a49fb-141">Dostępne warunki rezerwacji dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="a49fb-141">Available reservation terms for this resource.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a49fb-142">-Confirm</span></span>
<span data-ttu-id="a49fb-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a49fb-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a49fb-144">-WhatIf</span></span>
<span data-ttu-id="a49fb-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a49fb-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a49fb-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a49fb-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49fb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a49fb-147">CommonParameters</span></span>
<span data-ttu-id="a49fb-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a49fb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a49fb-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a49fb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a49fb-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a49fb-150">INPUTS</span></span>

### <span data-ttu-id="a49fb-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a49fb-151">None</span></span>

## <span data-ttu-id="a49fb-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a49fb-152">OUTPUTS</span></span>

### <span data-ttu-id="a49fb-153">Microsoft. Azure. Management. rezerwacje. modele. ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="a49fb-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="a49fb-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a49fb-154">NOTES</span></span>

## <span data-ttu-id="a49fb-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a49fb-155">RELATED LINKS</span></span>

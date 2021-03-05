---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 37be462c2af2c33987e6acd0118c3169b1e062d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000202"
---
# <span data-ttu-id="72916-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="72916-101">New-AzReservation</span></span>

## <span data-ttu-id="72916-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72916-102">SYNOPSIS</span></span>
<span data-ttu-id="72916-103">Zakup rezerwacji</span><span class="sxs-lookup"><span data-stu-id="72916-103">Purchase a reservation</span></span>

## <span data-ttu-id="72916-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72916-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72916-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="72916-105">DESCRIPTION</span></span>
<span data-ttu-id="72916-106">Kup wystąpienie rezerwacji i uzyskaj korzyść</span><span class="sxs-lookup"><span data-stu-id="72916-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="72916-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72916-107">EXAMPLES</span></span>

### <span data-ttu-id="72916-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72916-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="72916-109">Po obliczeniu ceny klient mógł przeczyścić wartość RI przez obliczenieCeny</span><span class="sxs-lookup"><span data-stu-id="72916-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="72916-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72916-110">PARAMETERS</span></span>

### <span data-ttu-id="72916-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="72916-111">-AppliedScope</span></span>
<span data-ttu-id="72916-112">Subskrypcja, do których zostanie zastosowana korzyść.</span><span class="sxs-lookup"><span data-stu-id="72916-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="72916-113">Wymagane, jeśli --applied-scope-type to Single.</span><span class="sxs-lookup"><span data-stu-id="72916-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="72916-114">Nie określaj, czy --applied-scope-type ma wartość Udostępnione.</span><span class="sxs-lookup"><span data-stu-id="72916-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="72916-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="72916-115">-AppliedScopeType</span></span>
<span data-ttu-id="72916-116">Typ zastosowanego zakresu w celu zaktualizowania rezerwacji przy użyciu wartości "Pojedyncza" lub "Udostępniona"</span><span class="sxs-lookup"><span data-stu-id="72916-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="72916-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="72916-117">-BillingPlan</span></span>
<span data-ttu-id="72916-118">Opcje planu rozliczeniowego dostępne dla tej wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="72916-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="72916-119">"Miesięczny" lub "Z góry"</span><span class="sxs-lookup"><span data-stu-id="72916-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="72916-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="72916-120">-BillingScopeId</span></span>
<span data-ttu-id="72916-121">Subskrypcja, która zostanie obciążona opłatami za zakup rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="72916-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="72916-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72916-122">-DefaultProfile</span></span>
<span data-ttu-id="72916-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="72916-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72916-124">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="72916-124">-DisplayName</span></span>
<span data-ttu-id="72916-125">Przyjazna nazwa, która umożliwia łatwe identyfikowanie rezerwacji przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="72916-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="72916-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="72916-126">-InstanceFlexibility</span></span>
<span data-ttu-id="72916-127">{{ Fill InstanceFlexibility Description }}</span><span class="sxs-lookup"><span data-stu-id="72916-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="72916-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="72916-128">-Location</span></span>
<span data-ttu-id="72916-129">Lokalizacja, w którym jest dostępna ta sku.</span><span class="sxs-lookup"><span data-stu-id="72916-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="72916-130">— Ilość</span><span class="sxs-lookup"><span data-stu-id="72916-130">-Quantity</span></span>
<span data-ttu-id="72916-131">Ilość produktu do obliczania ceny lub zakupów.</span><span class="sxs-lookup"><span data-stu-id="72916-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="72916-132">— Odnów</span><span class="sxs-lookup"><span data-stu-id="72916-132">-Renew</span></span>
<span data-ttu-id="72916-133">Ustawienie wartości true spowoduje automatyczne zakupienie nowej rezerwacji w dniu wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="72916-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="72916-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="72916-134">-ReservationOrderId</span></span>
<span data-ttu-id="72916-135">Obliczanie identyfikatora zamówienia rezerwacji, wygenerowanego przez zamówienie rezerwacji z rezerwacjami az.</span><span class="sxs-lookup"><span data-stu-id="72916-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="72916-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="72916-136">-ReservedResourceType</span></span>
<span data-ttu-id="72916-137">Typ zasobu, dla którego powinny zostać podane jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="72916-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="72916-138">- SKU</span><span class="sxs-lookup"><span data-stu-id="72916-138">-Sku</span></span>
<span data-ttu-id="72916-139">Nazwa sku</span><span class="sxs-lookup"><span data-stu-id="72916-139">Sku name</span></span>

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

### <span data-ttu-id="72916-140">— termin</span><span class="sxs-lookup"><span data-stu-id="72916-140">-Term</span></span>
<span data-ttu-id="72916-141">Dostępne warunki rezerwacji dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="72916-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="72916-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72916-142">-Confirm</span></span>
<span data-ttu-id="72916-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72916-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72916-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72916-144">-WhatIf</span></span>
<span data-ttu-id="72916-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72916-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72916-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="72916-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72916-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72916-147">CommonParameters</span></span>
<span data-ttu-id="72916-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72916-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72916-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72916-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72916-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72916-150">INPUTS</span></span>

### <span data-ttu-id="72916-151">Brak</span><span class="sxs-lookup"><span data-stu-id="72916-151">None</span></span>

## <span data-ttu-id="72916-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72916-152">OUTPUTS</span></span>

### <span data-ttu-id="72916-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="72916-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="72916-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72916-154">NOTES</span></span>

## <span data-ttu-id="72916-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72916-155">RELATED LINKS</span></span>

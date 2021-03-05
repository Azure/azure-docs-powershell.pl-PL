---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 3a06de95cedd0ea38fa38b2fb8784e553ae6f4d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000257"
---
# <span data-ttu-id="294d9-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="294d9-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="294d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="294d9-102">SYNOPSIS</span></span>
<span data-ttu-id="294d9-103">Uzyskaj ofertę dla rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="294d9-103">Get a quote for the reservation.</span></span> <span data-ttu-id="294d9-104">Te informacje są przekazywane `New-AzReservation` do zakupu.</span><span class="sxs-lookup"><span data-stu-id="294d9-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="294d9-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="294d9-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="294d9-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="294d9-106">DESCRIPTION</span></span>
<span data-ttu-id="294d9-107">Oblicz cenę za złożenie zamówienia rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="294d9-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="294d9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="294d9-108">EXAMPLES</span></span>

### <span data-ttu-id="294d9-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="294d9-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="294d9-110">Po pobierz katalog, klient może uzyskać produkt inny w zależności od lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="294d9-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="294d9-111">Używając tych informacji, sprawdź odpowiednio cenę</span><span class="sxs-lookup"><span data-stu-id="294d9-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="294d9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="294d9-112">PARAMETERS</span></span>

### <span data-ttu-id="294d9-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="294d9-113">-AppliedScope</span></span>
<span data-ttu-id="294d9-114">Subskrypcja, do których zostanie zastosowana korzyść.</span><span class="sxs-lookup"><span data-stu-id="294d9-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="294d9-115">Wymagane, jeśli --applied-scope-type to Single.</span><span class="sxs-lookup"><span data-stu-id="294d9-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="294d9-116">Nie określaj, czy --applied-scope-type ma wartość Udostępnione.</span><span class="sxs-lookup"><span data-stu-id="294d9-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="294d9-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="294d9-117">-AppliedScopeType</span></span>
<span data-ttu-id="294d9-118">Typ zastosowanego zakresu w celu zaktualizowania rezerwacji przy użyciu wartości "Pojedyncza" lub "Udostępniona"</span><span class="sxs-lookup"><span data-stu-id="294d9-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="294d9-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="294d9-119">-BillingPlan</span></span>
<span data-ttu-id="294d9-120">Opcje planu rozliczeniowego dostępne dla tej wersji SKU.</span><span class="sxs-lookup"><span data-stu-id="294d9-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="294d9-121">"Miesięczny" lub "Z góry"</span><span class="sxs-lookup"><span data-stu-id="294d9-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="294d9-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="294d9-122">-BillingScopeId</span></span>
<span data-ttu-id="294d9-123">Subskrypcja, która zostanie obciążona opłatami za zakup rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="294d9-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="294d9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294d9-124">-DefaultProfile</span></span>
<span data-ttu-id="294d9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="294d9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="294d9-126">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="294d9-126">-DisplayName</span></span>
<span data-ttu-id="294d9-127">Przyjazna nazwa, która umożliwia łatwe identyfikowanie rezerwacji przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="294d9-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="294d9-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="294d9-128">-InstanceFlexibility</span></span>
<span data-ttu-id="294d9-129">Typ elastyczności wystąpienia, za pomocą których można zaktualizować rezerwację.</span><span class="sxs-lookup"><span data-stu-id="294d9-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="294d9-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="294d9-130">-Location</span></span>
<span data-ttu-id="294d9-131">Lokalizacja, w którym jest dostępna ta sku.</span><span class="sxs-lookup"><span data-stu-id="294d9-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="294d9-132">— Ilość</span><span class="sxs-lookup"><span data-stu-id="294d9-132">-Quantity</span></span>
<span data-ttu-id="294d9-133">Ilość produktu do obliczania ceny lub zakupów.</span><span class="sxs-lookup"><span data-stu-id="294d9-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="294d9-134">— Odnów</span><span class="sxs-lookup"><span data-stu-id="294d9-134">-Renew</span></span>
<span data-ttu-id="294d9-135">Ustawienie wartości true spowoduje automatyczne zakupienie nowej rezerwacji w dniu wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="294d9-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="294d9-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="294d9-136">-ReservedResourceType</span></span>
<span data-ttu-id="294d9-137">Typ zasobu, dla którego powinny zostać podane jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="294d9-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="294d9-138">- SKU</span><span class="sxs-lookup"><span data-stu-id="294d9-138">-Sku</span></span>
<span data-ttu-id="294d9-139">Nazwa sku, uzyskiwanie listy sku przy użyciu polecenia az reservations catalog show</span><span class="sxs-lookup"><span data-stu-id="294d9-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="294d9-140">— termin</span><span class="sxs-lookup"><span data-stu-id="294d9-140">-Term</span></span>
<span data-ttu-id="294d9-141">Dostępne warunki rezerwacji dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="294d9-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="294d9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294d9-142">CommonParameters</span></span>
<span data-ttu-id="294d9-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="294d9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294d9-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="294d9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294d9-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="294d9-145">INPUTS</span></span>

### <span data-ttu-id="294d9-146">Brak</span><span class="sxs-lookup"><span data-stu-id="294d9-146">None</span></span>

## <span data-ttu-id="294d9-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="294d9-147">OUTPUTS</span></span>

### <span data-ttu-id="294d9-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="294d9-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="294d9-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="294d9-149">NOTES</span></span>

## <span data-ttu-id="294d9-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="294d9-150">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 073a059063198e91a1bbcc67814c01c1b786e7c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370092"
---
# <span data-ttu-id="39d5f-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="39d5f-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="39d5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="39d5f-103">Pobierz ofertę na rezerwację.</span><span class="sxs-lookup"><span data-stu-id="39d5f-103">Get a quote for the reservation.</span></span> <span data-ttu-id="39d5f-104">Jest to przekazywane do `New-AzReservation` zakupu.</span><span class="sxs-lookup"><span data-stu-id="39d5f-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="39d5f-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39d5f-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39d5f-106">Opis</span><span class="sxs-lookup"><span data-stu-id="39d5f-106">DESCRIPTION</span></span>
<span data-ttu-id="39d5f-107">Oblicz cenę doprowadzenia zlecenia rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="39d5f-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="39d5f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39d5f-108">EXAMPLES</span></span>

### <span data-ttu-id="39d5f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39d5f-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="39d5f-110">Po uzyskaniu wykazu klient może uzyskać inny produkt na podstawie lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="39d5f-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="39d5f-111">Korzystając z tych informacji, sprawdź poprawność ceny</span><span class="sxs-lookup"><span data-stu-id="39d5f-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="39d5f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39d5f-112">PARAMETERS</span></span>

### <span data-ttu-id="39d5f-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="39d5f-113">-AppliedScope</span></span>
<span data-ttu-id="39d5f-114">Abonament, na który zostaną zastosowane świadczenia.</span><span class="sxs-lookup"><span data-stu-id="39d5f-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="39d5f-115">Wymagane, jeśli--zastosowano-Scope-Type (jeden).</span><span class="sxs-lookup"><span data-stu-id="39d5f-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="39d5f-116">Nie określaj, czy--zastosowano-zakres-typ jest udostępniony.</span><span class="sxs-lookup"><span data-stu-id="39d5f-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="39d5f-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="39d5f-117">-AppliedScopeType</span></span>
<span data-ttu-id="39d5f-118">Typ zastosowanego zakresu w celu zaktualizowania rezerwacji za pomocą "jednego" lub "udostępnionego"</span><span class="sxs-lookup"><span data-stu-id="39d5f-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="39d5f-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="39d5f-119">-BillingPlan</span></span>
<span data-ttu-id="39d5f-120">Opcje planu rozliczeń dostępne dla tej jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="39d5f-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="39d5f-121">"Co miesiąc" lub "z przodu"</span><span class="sxs-lookup"><span data-stu-id="39d5f-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="39d5f-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="39d5f-122">-BillingScopeId</span></span>
<span data-ttu-id="39d5f-123">Abonament naliczany na potrzeby rezerwacji zakupów.</span><span class="sxs-lookup"><span data-stu-id="39d5f-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="39d5f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d5f-124">-DefaultProfile</span></span>
<span data-ttu-id="39d5f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39d5f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d5f-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="39d5f-126">-DisplayName</span></span>
<span data-ttu-id="39d5f-127">Przyjazna nazwa użytkownika w celu łatwego identyfikowania rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="39d5f-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="39d5f-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="39d5f-128">-InstanceFlexibility</span></span>
<span data-ttu-id="39d5f-129">Typ elastyczności wystąpienia w celu zaktualizowania rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="39d5f-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="39d5f-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="39d5f-130">-Location</span></span>
<span data-ttu-id="39d5f-131">Lokalizacja, w której dostępna jest jednostka SKU.</span><span class="sxs-lookup"><span data-stu-id="39d5f-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="39d5f-132">-Ilość</span><span class="sxs-lookup"><span data-stu-id="39d5f-132">-Quantity</span></span>
<span data-ttu-id="39d5f-133">Ilość produktu do obliczania ceny lub zakupu.</span><span class="sxs-lookup"><span data-stu-id="39d5f-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="39d5f-134">-Renew</span><span class="sxs-lookup"><span data-stu-id="39d5f-134">-Renew</span></span>
<span data-ttu-id="39d5f-135">Ustawienie wartości true spowoduje automatyczne zakupienie nowej rezerwacji w dniu daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="39d5f-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="39d5f-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="39d5f-136">-ReservedResourceType</span></span>
<span data-ttu-id="39d5f-137">Typ zasobu, dla którego należy podać jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="39d5f-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="39d5f-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="39d5f-138">-Sku</span></span>
<span data-ttu-id="39d5f-139">Nazwa jednostki SKU, uzyskiwanie listy SKU przy użyciu polecenia AZ rezerwacje wykazu Pokaż</span><span class="sxs-lookup"><span data-stu-id="39d5f-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="39d5f-140">-Term</span><span class="sxs-lookup"><span data-stu-id="39d5f-140">-Term</span></span>
<span data-ttu-id="39d5f-141">Dostępne warunki rezerwacji dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="39d5f-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="39d5f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d5f-142">CommonParameters</span></span>
<span data-ttu-id="39d5f-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d5f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d5f-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39d5f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d5f-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39d5f-145">INPUTS</span></span>

### <span data-ttu-id="39d5f-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="39d5f-146">None</span></span>

## <span data-ttu-id="39d5f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39d5f-147">OUTPUTS</span></span>

### <span data-ttu-id="39d5f-148">Microsoft. Azure. Management. rezerwacje. modele. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="39d5f-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="39d5f-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39d5f-149">NOTES</span></span>

## <span data-ttu-id="39d5f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39d5f-150">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221668"
---
# <span data-ttu-id="f6159-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="f6159-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="f6159-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6159-102">SYNOPSIS</span></span>
<span data-ttu-id="f6159-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="f6159-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="f6159-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6159-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6159-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6159-105">DESCRIPTION</span></span>
<span data-ttu-id="f6159-106">Oblicz cenę doprowadzenia zlecenia rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="f6159-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="f6159-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6159-107">EXAMPLES</span></span>

### <span data-ttu-id="f6159-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6159-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="f6159-109">Po uzyskaniu wykazu klient może uzyskać inny produkt na podstawie lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f6159-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="f6159-110">Korzystając z tych informacji, sprawdź poprawność ceny</span><span class="sxs-lookup"><span data-stu-id="f6159-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="f6159-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6159-111">PARAMETERS</span></span>

### <span data-ttu-id="f6159-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="f6159-112">-AppliedScope</span></span>
<span data-ttu-id="f6159-113">Abonament, na który zostaną zastosowane świadczenia.</span><span class="sxs-lookup"><span data-stu-id="f6159-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="f6159-114">Wymagane, jeśli--zastosowano-Scope-Type (jeden).</span><span class="sxs-lookup"><span data-stu-id="f6159-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="f6159-115">Nie określaj, czy--zastosowano-zakres-typ jest udostępniony.</span><span class="sxs-lookup"><span data-stu-id="f6159-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="f6159-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="f6159-116">-AppliedScopeType</span></span>
<span data-ttu-id="f6159-117">Typ zastosowanego zakresu w celu zaktualizowania rezerwacji za pomocą "jednego" lub "udostępnionego"</span><span class="sxs-lookup"><span data-stu-id="f6159-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="f6159-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="f6159-118">-BillingPlan</span></span>
<span data-ttu-id="f6159-119">Opcje planu rozliczeń dostępne dla tej jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="f6159-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="f6159-120">"Co miesiąc" lub "z przodu"</span><span class="sxs-lookup"><span data-stu-id="f6159-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="f6159-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="f6159-121">-BillingScopeId</span></span>
<span data-ttu-id="f6159-122">Abonament naliczany na potrzeby rezerwacji zakupów.</span><span class="sxs-lookup"><span data-stu-id="f6159-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="f6159-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6159-123">-DefaultProfile</span></span>
<span data-ttu-id="f6159-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6159-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6159-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f6159-125">-DisplayName</span></span>
<span data-ttu-id="f6159-126">Przyjazna nazwa użytkownika w celu łatwego identyfikowania rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="f6159-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="f6159-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="f6159-127">-InstanceFlexibility</span></span>
<span data-ttu-id="f6159-128">Typ elastyczności wystąpienia w celu zaktualizowania rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="f6159-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="f6159-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f6159-129">-Location</span></span>
<span data-ttu-id="f6159-130">Lokalizacja, w której dostępna jest jednostka SKU.</span><span class="sxs-lookup"><span data-stu-id="f6159-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="f6159-131">-Ilość</span><span class="sxs-lookup"><span data-stu-id="f6159-131">-Quantity</span></span>
<span data-ttu-id="f6159-132">Ilość produktu do obliczania ceny lub zakupu.</span><span class="sxs-lookup"><span data-stu-id="f6159-132">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="f6159-133">-Renew</span><span class="sxs-lookup"><span data-stu-id="f6159-133">-Renew</span></span>
<span data-ttu-id="f6159-134">Ustawienie wartości true spowoduje automatyczne zakupienie nowej rezerwacji w dniu daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="f6159-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="f6159-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="f6159-135">-ReservedResourceType</span></span>
<span data-ttu-id="f6159-136">Typ zasobu, dla którego należy podać jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="f6159-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="f6159-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="f6159-137">-Sku</span></span>
<span data-ttu-id="f6159-138">Nazwa jednostki SKU, uzyskiwanie listy SKU przy użyciu polecenia AZ rezerwacje wykazu Pokaż</span><span class="sxs-lookup"><span data-stu-id="f6159-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="f6159-139">-Term</span><span class="sxs-lookup"><span data-stu-id="f6159-139">-Term</span></span>
<span data-ttu-id="f6159-140">Dostępne warunki rezerwacji dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="f6159-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="f6159-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6159-141">CommonParameters</span></span>
<span data-ttu-id="f6159-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6159-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6159-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6159-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6159-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6159-144">INPUTS</span></span>

### <span data-ttu-id="f6159-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f6159-145">None</span></span>

## <span data-ttu-id="f6159-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6159-146">OUTPUTS</span></span>

### <span data-ttu-id="f6159-147">Microsoft. Azure. Management. rezerwacje. modele. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="f6159-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="f6159-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6159-148">NOTES</span></span>

## <span data-ttu-id="f6159-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6159-149">RELATED LINKS</span></span>

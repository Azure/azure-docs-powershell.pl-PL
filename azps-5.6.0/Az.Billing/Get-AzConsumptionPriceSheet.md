---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: 601048df040ed317f158d473ac484ce53529d20a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977594"
---
# <span data-ttu-id="61dc5-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="61dc5-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="61dc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="61dc5-103">Pobierz arkusze cenowe subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="61dc5-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="61dc5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61dc5-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61dc5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="61dc5-105">DESCRIPTION</span></span>
<span data-ttu-id="61dc5-106">Polecenie **cmdlet Get-AzConsumptionPriceSheet** pobiera arkusze cen subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="61dc5-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="61dc5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61dc5-107">EXAMPLES</span></span>

### <span data-ttu-id="61dc5-108">Przykład 1. Uzyskiwanie arkuszy cen</span><span class="sxs-lookup"><span data-stu-id="61dc5-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="61dc5-109">Przykład 2. Uzyskiwanie arkuszy cenowych z rozbudowaną ofertą MeterDetails</span><span class="sxs-lookup"><span data-stu-id="61dc5-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="61dc5-110">Przykład 3. Uzyskiwanie arkuszy cen dla parametru BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="61dc5-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### <span data-ttu-id="61dc5-111">Przykład 4. Uzyskiwanie 5 najlepszych rekordów arkuszy cen</span><span class="sxs-lookup"><span data-stu-id="61dc5-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## <span data-ttu-id="61dc5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61dc5-112">PARAMETERS</span></span>

### <span data-ttu-id="61dc5-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="61dc5-113">-BillingPeriodName</span></span>
<span data-ttu-id="61dc5-114">Nazwa konkretnego okresu rozliczeniowego w celu uzyskania arkuszy cen, z którym jest skojarzony.</span><span class="sxs-lookup"><span data-stu-id="61dc5-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="61dc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dc5-115">-DefaultProfile</span></span>
<span data-ttu-id="61dc5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61dc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61dc5-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="61dc5-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="61dc5-118">Rozwiń arkusze cen na podstawie szczegółów taryfowego.</span><span class="sxs-lookup"><span data-stu-id="61dc5-118">Expand the price sheets based on MeterDetails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dc5-119">— Na górze</span><span class="sxs-lookup"><span data-stu-id="61dc5-119">-Top</span></span>
<span data-ttu-id="61dc5-120">Określ maksymalną liczbę rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="61dc5-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dc5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dc5-121">CommonParameters</span></span>
<span data-ttu-id="61dc5-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61dc5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dc5-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61dc5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dc5-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61dc5-124">INPUTS</span></span>

### <span data-ttu-id="61dc5-125">Brak</span><span class="sxs-lookup"><span data-stu-id="61dc5-125">None</span></span>

## <span data-ttu-id="61dc5-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61dc5-126">OUTPUTS</span></span>

### <span data-ttu-id="61dc5-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="61dc5-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="61dc5-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61dc5-128">NOTES</span></span>

## <span data-ttu-id="61dc5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61dc5-129">RELATED LINKS</span></span>

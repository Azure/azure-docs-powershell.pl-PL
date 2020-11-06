---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionPriceSheet.md
ms.openlocfilehash: 46e38df713483b60735247c7fafe984fc5fb6d52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541792"
---
# <span data-ttu-id="d704e-101">Get-AzureRmConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="d704e-101">Get-AzureRmConsumptionPriceSheet</span></span>

## <span data-ttu-id="d704e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d704e-102">SYNOPSIS</span></span>
<span data-ttu-id="d704e-103">Pobierz arkusze cenowe subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d704e-103">Get price sheets of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d704e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d704e-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d704e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d704e-105">DESCRIPTION</span></span>
<span data-ttu-id="d704e-106">Polecenie cmdlet **Get-AzureRmConsumptionPriceSheet** pobiera arkusze cenowe subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d704e-106">The **Get-AzureRmConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="d704e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d704e-107">EXAMPLES</span></span>

### <span data-ttu-id="d704e-108">Przykład 1: Pobierz arkusze cen</span><span class="sxs-lookup"><span data-stu-id="d704e-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet
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

### <span data-ttu-id="d704e-109">Przykład 2: uzyskiwanie arkuszy cen z rozwinięciem MeterDetails</span><span class="sxs-lookup"><span data-stu-id="d704e-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -ExpandMeterDetail
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

### <span data-ttu-id="d704e-110">Przykład 3: uzyskiwanie arkuszy cenowych BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="d704e-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -BillingPeriodName 201712
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

### <span data-ttu-id="d704e-111">Przykład 4: pobieranie 5 pierwszych rekordów arkuszy cen</span><span class="sxs-lookup"><span data-stu-id="d704e-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -Top 5
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

## <span data-ttu-id="d704e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d704e-112">PARAMETERS</span></span>

### <span data-ttu-id="d704e-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="d704e-113">-BillingPeriodName</span></span>
<span data-ttu-id="d704e-114">Nazwa określonego okresu rozliczeniowego, w którym mają zostać powiązane arkusze cen.</span><span class="sxs-lookup"><span data-stu-id="d704e-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="d704e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d704e-115">-DefaultProfile</span></span>
<span data-ttu-id="d704e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d704e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d704e-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="d704e-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="d704e-118">Rozwiń arkusze cen na podstawie MeterDetails.</span><span class="sxs-lookup"><span data-stu-id="d704e-118">Expand the price sheets based on MeterDetails.</span></span>

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

### <span data-ttu-id="d704e-119">-Początek</span><span class="sxs-lookup"><span data-stu-id="d704e-119">-Top</span></span>
<span data-ttu-id="d704e-120">Określ maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="d704e-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="d704e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d704e-121">CommonParameters</span></span>
<span data-ttu-id="d704e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d704e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d704e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d704e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d704e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d704e-124">INPUTS</span></span>

### <span data-ttu-id="d704e-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d704e-125">None</span></span>

## <span data-ttu-id="d704e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d704e-126">OUTPUTS</span></span>

### <span data-ttu-id="d704e-127">Microsoft. Azure. Commands.. models. PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="d704e-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="d704e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d704e-128">NOTES</span></span>

## <span data-ttu-id="d704e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d704e-129">RELATED LINKS</span></span>

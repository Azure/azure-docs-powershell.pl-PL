---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 2694ce516b1bb3202fc194e1c1eec55610f7b92a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525229"
---
# <span data-ttu-id="9a4ad-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="9a4ad-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="9a4ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4ad-103">Pobierz szczegóły użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a4ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a4ad-104">SYNTAX</span></span>

### <span data-ttu-id="9a4ad-105">Abonament (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9a4ad-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a4ad-106">Fakturowa</span><span class="sxs-lookup"><span data-stu-id="9a4ad-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a4ad-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="9a4ad-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a4ad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9a4ad-108">DESCRIPTION</span></span>
<span data-ttu-id="9a4ad-109">Polecenie cmdlet **Get-AzureRmConsumptionUsageDetail** pobiera dane dotyczące użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="9a4ad-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a4ad-110">EXAMPLES</span></span>

### <span data-ttu-id="9a4ad-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a4ad-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="9a4ad-112">Pobierz szczegóły użycia faktury o określonej nazwie i Dołącz Właściwość MeterDetails w wyniku.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="9a4ad-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9a4ad-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="9a4ad-114">Pobierz szczegóły użycia okresu rozliczeniowego o określonej nazwie i Dołącz Właściwość AdditionalProperties w wyniku.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="9a4ad-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9a4ad-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="9a4ad-116">Pobierz szczegóły użycia subskrypcji z zakresu od 2017-01-17 do 2017-01-19.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="9a4ad-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a4ad-117">PARAMETERS</span></span>

### <span data-ttu-id="9a4ad-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="9a4ad-118">-BillingPeriodName</span></span>
<span data-ttu-id="9a4ad-119">Nazwa określonego okresu rozliczeniowego, w którym mają zostać udostępnione dane dotyczące użycia.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4ad-120">-DefaultProfile</span></span>
<span data-ttu-id="9a4ad-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9a4ad-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9a4ad-122">-EndDate</span></span>
<span data-ttu-id="9a4ad-123">Data zakończenia (w formacie UTC) użycia.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-123">The end date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-124">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="9a4ad-124">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="9a4ad-125">Dodaj dodatkowe właściwości do użycia.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-125">Include additional properties in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-126">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="9a4ad-126">-IncludeMeterDetails</span></span>
<span data-ttu-id="9a4ad-127">Dołączanie szczegółów miernika do użycia.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-127">Include meter details in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-128">-Invoicename</span><span class="sxs-lookup"><span data-stu-id="9a4ad-128">-InvoiceName</span></span>
<span data-ttu-id="9a4ad-129">Nazwa konkretnej faktury, w której mają zostać udostępnione dane dotyczące użycia.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-129">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9a4ad-130">-MaxCount</span></span>
<span data-ttu-id="9a4ad-131">Określ maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-131">Determine the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-132">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="9a4ad-132">-StartDate</span></span>
<span data-ttu-id="9a4ad-133">Data rozpoczęcia (w formacie UTC) użycia.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-133">The start date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4ad-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4ad-134">CommonParameters</span></span>
<span data-ttu-id="9a4ad-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4ad-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4ad-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a4ad-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4ad-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a4ad-137">INPUTS</span></span>

### <span data-ttu-id="9a4ad-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9a4ad-138">None</span></span>

## <span data-ttu-id="9a4ad-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a4ad-139">OUTPUTS</span></span>

### <span data-ttu-id="9a4ad-140">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Commands. MODELES. PSUsageDetail; Microsoft. Azure. Commands; wersja = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9a4ad-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9a4ad-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a4ad-141">NOTES</span></span>

## <span data-ttu-id="9a4ad-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a4ad-142">RELATED LINKS</span></span>


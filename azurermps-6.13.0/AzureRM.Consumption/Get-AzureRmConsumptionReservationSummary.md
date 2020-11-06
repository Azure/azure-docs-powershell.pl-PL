---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationSummary.md
ms.openlocfilehash: 18f12e6ccf7f43aa832c00864192142457f45520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548803"
---
# <span data-ttu-id="56299-101">Get-AzureRmConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="56299-101">Get-AzureRmConsumptionReservationSummary</span></span>

## <span data-ttu-id="56299-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56299-102">SYNOPSIS</span></span>
<span data-ttu-id="56299-103">Pobierz podsumowania rezerwacji codziennie lub miesięcznym ziarnem.</span><span class="sxs-lookup"><span data-stu-id="56299-103">Get reservation summaries for daily or monthly grain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56299-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56299-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56299-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56299-105">DESCRIPTION</span></span>
<span data-ttu-id="56299-106">Polecenie cmdlet **Get-AzureRmConsumptionReservationSummay** pobiera podsumowania rezerwacji codziennie lub miesięcznym ziarnem.</span><span class="sxs-lookup"><span data-stu-id="56299-106">The **Get-AzureRmConsumptionReservationSummay** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="56299-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56299-107">EXAMPLES</span></span>

### <span data-ttu-id="56299-108">Przykład 1: pobieranie podsumowań rezerwacji z identyfikatorem zamówienia rezerwacji dla ziarna miesięcznego</span><span class="sxs-lookup"><span data-stu-id="56299-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="56299-109">Przykład 2: uzyskiwanie podsumowań rezerwacji za pomocą identyfikatora zamówienia rezerwacji i identyfikatora rezerwacji dla ziarna miesięcznego</span><span class="sxs-lookup"><span data-stu-id="56299-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="56299-110">Przykład 3: uzyskiwanie podsumowań rezerwacji z identyfikatorem zamówienia rezerwacji dla określonego ziarna dziennego w zakresie dat</span><span class="sxs-lookup"><span data-stu-id="56299-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="56299-111">Przykład 4: pobieranie podsumowań rezerwacji z identyfikatorem zamówienia rezerwacji i identyfikatorem rezerwacji dla określonego ziarna dziennego w zakresie dat</span><span class="sxs-lookup"><span data-stu-id="56299-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="56299-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56299-112">PARAMETERS</span></span>

### <span data-ttu-id="56299-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56299-113">-DefaultProfile</span></span>
<span data-ttu-id="56299-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56299-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56299-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="56299-115">-EndDate</span></span>
<span data-ttu-id="56299-116">Dane końcowe (RRRR-MM-DD in UTC) podsumowania rezerwacji są wymagane tylko w przypadku ziarna dziennego.</span><span class="sxs-lookup"><span data-stu-id="56299-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56299-117">-Ziarno</span><span class="sxs-lookup"><span data-stu-id="56299-117">-Grain</span></span>
<span data-ttu-id="56299-118">Ziarno czasu w podsumowaniu rezerwacji może być codzienne lub comiesięczne.</span><span class="sxs-lookup"><span data-stu-id="56299-118">The time grain of the reservation summaryy, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56299-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="56299-119">-ReservationId</span></span>
<span data-ttu-id="56299-120">Identyfikator rezerwacji w zamówieniu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="56299-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="56299-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="56299-121">-ReservationOrderId</span></span>
<span data-ttu-id="56299-122">Identyfikator zakupu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="56299-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="56299-123">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="56299-123">-StartDate</span></span>
<span data-ttu-id="56299-124">Dane początkowe (RRRR-MM-DD in UTC) podsumowania rezerwacji są wymagane tylko w przypadku ziarna dziennego.</span><span class="sxs-lookup"><span data-stu-id="56299-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56299-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56299-125">CommonParameters</span></span>
<span data-ttu-id="56299-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56299-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56299-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56299-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56299-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56299-128">INPUTS</span></span>

### <span data-ttu-id="56299-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="56299-129">None</span></span>

## <span data-ttu-id="56299-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56299-130">OUTPUTS</span></span>

### <span data-ttu-id="56299-131">Microsoft. Azure. Commands.. models. PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="56299-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="56299-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56299-132">NOTES</span></span>

## <span data-ttu-id="56299-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56299-133">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: 3b59aaf537c544a53a1e1cccbb09c1964f6662fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706627"
---
# <span data-ttu-id="9feab-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="9feab-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="9feab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9feab-102">SYNOPSIS</span></span>
<span data-ttu-id="9feab-103">Pobierz podsumowania rezerwacji codziennie lub miesięcznym ziarnem.</span><span class="sxs-lookup"><span data-stu-id="9feab-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="9feab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9feab-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9feab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9feab-105">DESCRIPTION</span></span>
<span data-ttu-id="9feab-106">Polecenie cmdlet **Get-AzConsumptionReservationSummary** pobiera podsumowania rezerwacji codziennie lub miesięcznym ziarnem.</span><span class="sxs-lookup"><span data-stu-id="9feab-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="9feab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9feab-107">EXAMPLES</span></span>

### <span data-ttu-id="9feab-108">Przykład 1: pobieranie podsumowań rezerwacji z identyfikatorem zamówienia rezerwacji dla ziarna miesięcznego</span><span class="sxs-lookup"><span data-stu-id="9feab-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
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

### <span data-ttu-id="9feab-109">Przykład 2: uzyskiwanie podsumowań rezerwacji za pomocą identyfikatora zamówienia rezerwacji i identyfikatora rezerwacji dla ziarna miesięcznego</span><span class="sxs-lookup"><span data-stu-id="9feab-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
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

### <span data-ttu-id="9feab-110">Przykład 3: uzyskiwanie podsumowań rezerwacji z identyfikatorem zamówienia rezerwacji dla określonego ziarna dziennego w zakresie dat</span><span class="sxs-lookup"><span data-stu-id="9feab-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
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

### <span data-ttu-id="9feab-111">Przykład 4: pobieranie podsumowań rezerwacji z identyfikatorem zamówienia rezerwacji i identyfikatorem rezerwacji dla określonego ziarna dziennego w zakresie dat</span><span class="sxs-lookup"><span data-stu-id="9feab-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
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

## <span data-ttu-id="9feab-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9feab-112">PARAMETERS</span></span>

### <span data-ttu-id="9feab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9feab-113">-DefaultProfile</span></span>
<span data-ttu-id="9feab-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9feab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9feab-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9feab-115">-EndDate</span></span>
<span data-ttu-id="9feab-116">Dane końcowe (RRRR-MM-DD in UTC) podsumowania rezerwacji są wymagane tylko w przypadku ziarna dziennego.</span><span class="sxs-lookup"><span data-stu-id="9feab-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="9feab-117">-Ziarno</span><span class="sxs-lookup"><span data-stu-id="9feab-117">-Grain</span></span>
<span data-ttu-id="9feab-118">Ziarno czasu z podsumowaniem rezerwacji może być codzienne lub comiesięczne.</span><span class="sxs-lookup"><span data-stu-id="9feab-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

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

### <span data-ttu-id="9feab-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="9feab-119">-ReservationId</span></span>
<span data-ttu-id="9feab-120">Identyfikator rezerwacji w zamówieniu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="9feab-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="9feab-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9feab-121">-ReservationOrderId</span></span>
<span data-ttu-id="9feab-122">Identyfikator zakupu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="9feab-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="9feab-123">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="9feab-123">-StartDate</span></span>
<span data-ttu-id="9feab-124">Dane początkowe (RRRR-MM-DD in UTC) podsumowania rezerwacji są wymagane tylko w przypadku ziarna dziennego.</span><span class="sxs-lookup"><span data-stu-id="9feab-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="9feab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9feab-125">CommonParameters</span></span>
<span data-ttu-id="9feab-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9feab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9feab-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9feab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9feab-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9feab-128">INPUTS</span></span>

### <span data-ttu-id="9feab-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9feab-129">None</span></span>

## <span data-ttu-id="9feab-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9feab-130">OUTPUTS</span></span>

### <span data-ttu-id="9feab-131">Microsoft. Azure. Commands.. models. PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="9feab-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="9feab-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9feab-132">NOTES</span></span>

## <span data-ttu-id="9feab-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9feab-133">RELATED LINKS</span></span>
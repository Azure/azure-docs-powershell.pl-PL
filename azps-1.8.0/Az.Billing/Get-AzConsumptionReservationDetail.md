---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 0776e824d9463a0577f64f2b19f0d71ece29cfa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869267"
---
# <span data-ttu-id="c075f-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="c075f-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="c075f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c075f-102">SYNOPSIS</span></span>
<span data-ttu-id="c075f-103">Uzyskaj szczegóły rezerwacji dla podanego zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="c075f-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="c075f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c075f-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c075f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c075f-105">DESCRIPTION</span></span>
<span data-ttu-id="c075f-106">Polecenie cmdlet **Get-AzConsumptionReservationDetail** pobiera szczegóły rezerwacji dla określonego zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="c075f-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="c075f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c075f-107">EXAMPLES</span></span>

### <span data-ttu-id="c075f-108">Przykład 1: pobieranie szczegółów rezerwacji z identyfikatorem zamówienia rezerwacji dla określonego zakresu dat</span><span class="sxs-lookup"><span data-stu-id="c075f-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="c075f-109">Przykład 2: pobieranie szczegółów rezerwacji z identyfikatorem zamówienia rezerwacji i identyfikatorem rezerwacji dla określonego zakresu dat</span><span class="sxs-lookup"><span data-stu-id="c075f-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="c075f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c075f-110">PARAMETERS</span></span>

### <span data-ttu-id="c075f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c075f-111">-DefaultProfile</span></span>
<span data-ttu-id="c075f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c075f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c075f-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c075f-113">-EndDate</span></span>
<span data-ttu-id="c075f-114">Dane końcowe (RRRR-MM-DD in UTC) szczegółów rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="c075f-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c075f-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="c075f-115">-ReservationId</span></span>
<span data-ttu-id="c075f-116">Identyfikator rezerwacji w zamówieniu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="c075f-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="c075f-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c075f-117">-ReservationOrderId</span></span>
<span data-ttu-id="c075f-118">Identyfikator zakupu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="c075f-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="c075f-119">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="c075f-119">-StartDate</span></span>
<span data-ttu-id="c075f-120">Dane początkowe (RRRR-MM-DD in UTC) szczegółów rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="c075f-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c075f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c075f-121">CommonParameters</span></span>
<span data-ttu-id="c075f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c075f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c075f-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c075f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c075f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c075f-124">INPUTS</span></span>

### <span data-ttu-id="c075f-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c075f-125">None</span></span>

## <span data-ttu-id="c075f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c075f-126">OUTPUTS</span></span>

### <span data-ttu-id="c075f-127">Microsoft. Azure. Commands.. models. PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="c075f-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="c075f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c075f-128">NOTES</span></span>

## <span data-ttu-id="c075f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c075f-129">RELATED LINKS</span></span>

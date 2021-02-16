---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 2a49cb88fc25643cd26e7ed75d226b8abf6ee50f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199466"
---
# <span data-ttu-id="a3688-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="a3688-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="a3688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3688-102">SYNOPSIS</span></span>
<span data-ttu-id="a3688-103">Uzyskaj szczegóły rezerwacji dla podanego zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="a3688-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="a3688-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3688-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3688-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3688-105">DESCRIPTION</span></span>
<span data-ttu-id="a3688-106">Polecenie **cmdlet Get-AzConsumptionReservationDetail** pobiera szczegóły rezerwacji dla podanego zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="a3688-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="a3688-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3688-107">EXAMPLES</span></span>

### <span data-ttu-id="a3688-108">Przykład 1. Uzyskiwanie szczegółów rezerwacji z identyfikatorem zamówienia rezerwacji dla podanego zakresu dat</span><span class="sxs-lookup"><span data-stu-id="a3688-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
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

### <span data-ttu-id="a3688-109">Przykład 2. Uzyskiwanie szczegółów rezerwacji z identyfikatorem zamówienia rezerwacji i identyfikatorem rezerwacji dla podanego zakresu dat</span><span class="sxs-lookup"><span data-stu-id="a3688-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
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

## <span data-ttu-id="a3688-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3688-110">PARAMETERS</span></span>

### <span data-ttu-id="a3688-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3688-111">-DefaultProfile</span></span>
<span data-ttu-id="a3688-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3688-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3688-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a3688-113">-EndDate</span></span>
<span data-ttu-id="a3688-114">Dane końcowe (YYYY-MM-DD w czasie UTC) szczegółów rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="a3688-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="a3688-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a3688-115">-ReservationId</span></span>
<span data-ttu-id="a3688-116">Identyfikator rezerwacji w ramach zamówienia rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="a3688-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="a3688-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a3688-117">-ReservationOrderId</span></span>
<span data-ttu-id="a3688-118">Identyfikator zakupu rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="a3688-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="a3688-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a3688-119">-StartDate</span></span>
<span data-ttu-id="a3688-120">Dane rozpoczęcia (YYYY-MM-DD w czasie UTC) szczegółów rezerwacji.</span><span class="sxs-lookup"><span data-stu-id="a3688-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="a3688-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3688-121">CommonParameters</span></span>
<span data-ttu-id="a3688-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3688-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3688-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3688-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3688-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3688-124">INPUTS</span></span>

### <span data-ttu-id="a3688-125">Brak</span><span class="sxs-lookup"><span data-stu-id="a3688-125">None</span></span>

## <span data-ttu-id="a3688-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3688-126">OUTPUTS</span></span>

### <span data-ttu-id="a3688-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="a3688-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="a3688-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3688-128">NOTES</span></span>

## <span data-ttu-id="a3688-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3688-129">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524965"
---
# <span data-ttu-id="7cc7c-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="7cc7c-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="7cc7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cc7c-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc7c-103">Pobieranie listy `Reservation` s w określonym zamówieniu rezerwacji</span><span class="sxs-lookup"><span data-stu-id="7cc7c-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cc7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cc7c-104">SYNTAX</span></span>

### <span data-ttu-id="7cc7c-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7cc7c-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="7cc7c-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="7cc7c-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="7cc7c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7cc7c-107">DESCRIPTION</span></span>
<span data-ttu-id="7cc7c-108">Lista `Reservation` s w ramach jednej z nich `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="7cc7c-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="7cc7c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cc7c-109">EXAMPLES</span></span>

### <span data-ttu-id="7cc7c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7cc7c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="7cc7c-111">Lista `Reservation` s w określonym czasie `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="7cc7c-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="7cc7c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7cc7c-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="7cc7c-113">Uzyskiwanie szczegółowych `Reservation` informacji.</span><span class="sxs-lookup"><span data-stu-id="7cc7c-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="7cc7c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cc7c-114">PARAMETERS</span></span>

### <span data-ttu-id="7cc7c-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="7cc7c-115">-ReservationId</span></span>
<span data-ttu-id="7cc7c-116">Identyfikator `Reservation` lokalizacji do wyszukania</span><span class="sxs-lookup"><span data-stu-id="7cc7c-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc7c-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="7cc7c-117">-ReservationOrder</span></span>
<span data-ttu-id="7cc7c-118">Parametr obiektu potoku `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7cc7c-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc7c-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="7cc7c-119">-ReservationOrderId</span></span>
<span data-ttu-id="7cc7c-120">Identyfikator `ReservationOrder` zawierający `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="7cc7c-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="7cc7c-121">Wymagane.</span><span class="sxs-lookup"><span data-stu-id="7cc7c-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc7c-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="7cc7c-122">-ReservationOrderPage</span></span>
<span data-ttu-id="7cc7c-123">Parametr obiektu potoku `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7cc7c-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc7c-124">CommonParameters</span></span>
<span data-ttu-id="7cc7c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc7c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc7c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc7c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cc7c-127">INPUTS</span></span>

### <span data-ttu-id="7cc7c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7cc7c-128">System.String</span></span>
<span data-ttu-id="7cc7c-129">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrder Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="7cc7c-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="7cc7c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cc7c-130">OUTPUTS</span></span>

### <span data-ttu-id="7cc7c-131">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="7cc7c-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="7cc7c-132">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="7cc7c-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="7cc7c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cc7c-133">NOTES</span></span>

## <span data-ttu-id="7cc7c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cc7c-134">RELATED LINKS</span></span>


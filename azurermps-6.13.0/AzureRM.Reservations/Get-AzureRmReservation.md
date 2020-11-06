---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526077"
---
# <span data-ttu-id="3aa08-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="3aa08-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="3aa08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3aa08-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa08-103">Pobieranie listy `Reservation` s w określonym zamówieniu rezerwacji</span><span class="sxs-lookup"><span data-stu-id="3aa08-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aa08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3aa08-104">SYNTAX</span></span>

### <span data-ttu-id="3aa08-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3aa08-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3aa08-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="3aa08-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3aa08-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="3aa08-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aa08-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3aa08-108">DESCRIPTION</span></span>
<span data-ttu-id="3aa08-109">Lista `Reservation` s w ramach jednej z nich `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="3aa08-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="3aa08-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3aa08-110">EXAMPLES</span></span>

### <span data-ttu-id="3aa08-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3aa08-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="3aa08-112">Lista `Reservation` s w określonym czasie `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="3aa08-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="3aa08-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3aa08-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="3aa08-114">Uzyskiwanie szczegółowych `Reservation` informacji.</span><span class="sxs-lookup"><span data-stu-id="3aa08-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="3aa08-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3aa08-115">PARAMETERS</span></span>

### <span data-ttu-id="3aa08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa08-116">-DefaultProfile</span></span>
<span data-ttu-id="3aa08-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aa08-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="3aa08-118">-ReservationId</span></span>
<span data-ttu-id="3aa08-119">Identyfikator `Reservation` lokalizacji do wyszukania</span><span class="sxs-lookup"><span data-stu-id="3aa08-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa08-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="3aa08-120">-ReservationOrder</span></span>
<span data-ttu-id="3aa08-121">Parametr obiektu potoku `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="3aa08-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa08-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3aa08-122">-ReservationOrderId</span></span>
<span data-ttu-id="3aa08-123">Identyfikator `ReservationOrder` zawierający `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="3aa08-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="3aa08-124">Wymagane.</span><span class="sxs-lookup"><span data-stu-id="3aa08-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa08-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="3aa08-125">-ReservationOrderPage</span></span>
<span data-ttu-id="3aa08-126">Parametr obiektu potoku `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="3aa08-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa08-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa08-127">CommonParameters</span></span>
<span data-ttu-id="3aa08-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa08-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa08-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa08-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa08-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aa08-130">INPUTS</span></span>

### <span data-ttu-id="3aa08-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3aa08-131">System.Guid</span></span>

### <span data-ttu-id="3aa08-132">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="3aa08-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="3aa08-133">Parametry: ReservationOrder (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3aa08-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="3aa08-134">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="3aa08-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="3aa08-135">Parametry: ReservationOrderPage (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3aa08-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="3aa08-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3aa08-136">OUTPUTS</span></span>

### <span data-ttu-id="3aa08-137">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="3aa08-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="3aa08-138">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="3aa08-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="3aa08-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3aa08-139">NOTES</span></span>

## <span data-ttu-id="3aa08-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3aa08-140">RELATED LINKS</span></span>

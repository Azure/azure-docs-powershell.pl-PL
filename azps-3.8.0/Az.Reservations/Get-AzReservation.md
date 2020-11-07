---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895973"
---
# <span data-ttu-id="4eb19-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="4eb19-101">Get-AzReservation</span></span>

## <span data-ttu-id="4eb19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4eb19-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb19-103">Pobieranie listy `Reservation` s w określonym zamówieniu rezerwacji</span><span class="sxs-lookup"><span data-stu-id="4eb19-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="4eb19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4eb19-104">SYNTAX</span></span>

### <span data-ttu-id="4eb19-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4eb19-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb19-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="4eb19-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb19-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="4eb19-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4eb19-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4eb19-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb19-109">Lista `Reservation` s w ramach jednej z nich `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="4eb19-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="4eb19-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4eb19-110">EXAMPLES</span></span>

### <span data-ttu-id="4eb19-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4eb19-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="4eb19-112">Lista `Reservation` s w określonym czasie `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="4eb19-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="4eb19-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4eb19-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="4eb19-114">Uzyskiwanie szczegółowych `Reservation` informacji.</span><span class="sxs-lookup"><span data-stu-id="4eb19-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="4eb19-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4eb19-115">PARAMETERS</span></span>

### <span data-ttu-id="4eb19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb19-116">-DefaultProfile</span></span>
<span data-ttu-id="4eb19-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4eb19-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb19-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="4eb19-118">-ReservationId</span></span>
<span data-ttu-id="4eb19-119">Identyfikator `Reservation` lokalizacji do wyszukania</span><span class="sxs-lookup"><span data-stu-id="4eb19-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="4eb19-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="4eb19-120">-ReservationOrder</span></span>
<span data-ttu-id="4eb19-121">Parametr obiektu potoku `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="4eb19-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="4eb19-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="4eb19-122">-ReservationOrderId</span></span>
<span data-ttu-id="4eb19-123">Identyfikator `ReservationOrder` zawierający `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="4eb19-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="4eb19-124">Wymagane.</span><span class="sxs-lookup"><span data-stu-id="4eb19-124">Required.</span></span>

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

### <span data-ttu-id="4eb19-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="4eb19-125">-ReservationOrderPage</span></span>
<span data-ttu-id="4eb19-126">Parametr obiektu potoku `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="4eb19-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="4eb19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb19-127">CommonParameters</span></span>
<span data-ttu-id="4eb19-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb19-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4eb19-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb19-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4eb19-130">INPUTS</span></span>

### <span data-ttu-id="4eb19-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4eb19-131">System.Guid</span></span>

### <span data-ttu-id="4eb19-132">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="4eb19-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="4eb19-133">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="4eb19-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="4eb19-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4eb19-134">OUTPUTS</span></span>

### <span data-ttu-id="4eb19-135">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="4eb19-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="4eb19-136">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="4eb19-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="4eb19-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4eb19-137">NOTES</span></span>

## <span data-ttu-id="4eb19-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4eb19-138">RELATED LINKS</span></span>

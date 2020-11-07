---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: d7eab73fbe6bed4a51df7c5056a0dc52787de845
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708452"
---
# <span data-ttu-id="b350c-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="b350c-101">Get-AzReservation</span></span>

## <span data-ttu-id="b350c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b350c-102">SYNOPSIS</span></span>
<span data-ttu-id="b350c-103">Pobieranie listy `Reservation` s w określonym zamówieniu rezerwacji</span><span class="sxs-lookup"><span data-stu-id="b350c-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="b350c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b350c-104">SYNTAX</span></span>

### <span data-ttu-id="b350c-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b350c-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b350c-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="b350c-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b350c-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="b350c-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b350c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b350c-108">DESCRIPTION</span></span>
<span data-ttu-id="b350c-109">Lista `Reservation` s w ramach jednej z nich `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="b350c-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="b350c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b350c-110">EXAMPLES</span></span>

### <span data-ttu-id="b350c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b350c-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="b350c-112">Lista `Reservation` s w określonym czasie `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="b350c-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="b350c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b350c-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="b350c-114">Uzyskiwanie szczegółowych `Reservation` informacji.</span><span class="sxs-lookup"><span data-stu-id="b350c-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="b350c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b350c-115">PARAMETERS</span></span>

### <span data-ttu-id="b350c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b350c-116">-DefaultProfile</span></span>
<span data-ttu-id="b350c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b350c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b350c-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="b350c-118">-ReservationId</span></span>
<span data-ttu-id="b350c-119">Identyfikator `Reservation` lokalizacji do wyszukania</span><span class="sxs-lookup"><span data-stu-id="b350c-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="b350c-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="b350c-120">-ReservationOrder</span></span>
<span data-ttu-id="b350c-121">Parametr obiektu potoku `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="b350c-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="b350c-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="b350c-122">-ReservationOrderId</span></span>
<span data-ttu-id="b350c-123">Identyfikator `ReservationOrder` zawierający `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="b350c-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="b350c-124">Wymagane.</span><span class="sxs-lookup"><span data-stu-id="b350c-124">Required.</span></span>

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

### <span data-ttu-id="b350c-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="b350c-125">-ReservationOrderPage</span></span>
<span data-ttu-id="b350c-126">Parametr obiektu potoku `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="b350c-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="b350c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b350c-127">CommonParameters</span></span>
<span data-ttu-id="b350c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b350c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b350c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b350c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b350c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b350c-130">INPUTS</span></span>

### <span data-ttu-id="b350c-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b350c-131">System.Guid</span></span>

### <span data-ttu-id="b350c-132">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="b350c-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="b350c-133">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="b350c-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="b350c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b350c-134">OUTPUTS</span></span>

### <span data-ttu-id="b350c-135">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="b350c-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="b350c-136">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="b350c-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="b350c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b350c-137">NOTES</span></span>

## <span data-ttu-id="b350c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b350c-138">RELATED LINKS</span></span>

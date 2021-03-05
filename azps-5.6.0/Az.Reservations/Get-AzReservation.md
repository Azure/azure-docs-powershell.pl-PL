---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 427e715e055cd909d204f92aedd58eca9d7db0f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000314"
---
# <span data-ttu-id="d4c54-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="d4c54-101">Get-AzReservation</span></span>

## <span data-ttu-id="d4c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4c54-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c54-103">`Reservation`Zamów w danym zamówieniu rezerwacji</span><span class="sxs-lookup"><span data-stu-id="d4c54-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="d4c54-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d4c54-104">SYNTAX</span></span>

### <span data-ttu-id="d4c54-105">CommandLine (Default)</span><span class="sxs-lookup"><span data-stu-id="d4c54-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4c54-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d4c54-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4c54-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="d4c54-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4c54-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d4c54-108">DESCRIPTION</span></span>
<span data-ttu-id="d4c54-109">Lista `Reservation` s w jednym. `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d4c54-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="d4c54-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d4c54-110">EXAMPLES</span></span>

### <span data-ttu-id="d4c54-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4c54-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="d4c54-112">Lista `Reservation` s w określonym `ReservationOrder` zakresie.</span><span class="sxs-lookup"><span data-stu-id="d4c54-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="d4c54-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d4c54-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="d4c54-114">Uzyskaj szczegółowe `Reservation` informacje.</span><span class="sxs-lookup"><span data-stu-id="d4c54-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="d4c54-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4c54-115">PARAMETERS</span></span>

### <span data-ttu-id="d4c54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c54-116">-DefaultProfile</span></span>
<span data-ttu-id="d4c54-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c54-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c54-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d4c54-118">-ReservationId</span></span>
<span data-ttu-id="d4c54-119">Identyfikator `Reservation` tematu do oglądu</span><span class="sxs-lookup"><span data-stu-id="d4c54-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="d4c54-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d4c54-120">-ReservationOrder</span></span>
<span data-ttu-id="d4c54-121">Parametr obiektu Pipe dla `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d4c54-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="d4c54-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d4c54-122">-ReservationOrderId</span></span>
<span data-ttu-id="d4c54-123">Identyfikator, `ReservationOrder` który zawiera . `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d4c54-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="d4c54-124">Wymagane.</span><span class="sxs-lookup"><span data-stu-id="d4c54-124">Required.</span></span>

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

### <span data-ttu-id="d4c54-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d4c54-125">-ReservationOrderPage</span></span>
<span data-ttu-id="d4c54-126">Parametr obiektu Pipe dla `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d4c54-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="d4c54-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c54-127">CommonParameters</span></span>
<span data-ttu-id="d4c54-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c54-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c54-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4c54-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c54-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4c54-130">INPUTS</span></span>

### <span data-ttu-id="d4c54-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d4c54-131">System.Guid</span></span>

### <span data-ttu-id="d4c54-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d4c54-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="d4c54-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d4c54-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="d4c54-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4c54-134">OUTPUTS</span></span>

### <span data-ttu-id="d4c54-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="d4c54-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="d4c54-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="d4c54-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d4c54-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d4c54-137">NOTES</span></span>

## <span data-ttu-id="d4c54-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4c54-138">RELATED LINKS</span></span>

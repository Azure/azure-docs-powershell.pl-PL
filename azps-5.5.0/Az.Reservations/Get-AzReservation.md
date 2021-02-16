---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242627"
---
# <span data-ttu-id="e86f2-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="e86f2-101">Get-AzReservation</span></span>

## <span data-ttu-id="e86f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e86f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e86f2-103">`Reservation`Zamów w danym zamówieniu rezerwacji</span><span class="sxs-lookup"><span data-stu-id="e86f2-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="e86f2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e86f2-104">SYNTAX</span></span>

### <span data-ttu-id="e86f2-105">CommandLine (Default)</span><span class="sxs-lookup"><span data-stu-id="e86f2-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e86f2-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e86f2-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e86f2-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="e86f2-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e86f2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e86f2-108">DESCRIPTION</span></span>
<span data-ttu-id="e86f2-109">Lista `Reservation` s w jednym. `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e86f2-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="e86f2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e86f2-110">EXAMPLES</span></span>

### <span data-ttu-id="e86f2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e86f2-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="e86f2-112">Lista `Reservation` s w określonym `ReservationOrder` zakresie.</span><span class="sxs-lookup"><span data-stu-id="e86f2-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="e86f2-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e86f2-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="e86f2-114">Uzyskaj szczegółowe `Reservation` informacje.</span><span class="sxs-lookup"><span data-stu-id="e86f2-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="e86f2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e86f2-115">PARAMETERS</span></span>

### <span data-ttu-id="e86f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e86f2-116">-DefaultProfile</span></span>
<span data-ttu-id="e86f2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e86f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e86f2-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="e86f2-118">-ReservationId</span></span>
<span data-ttu-id="e86f2-119">Identyfikator `Reservation` tematu do oglądu</span><span class="sxs-lookup"><span data-stu-id="e86f2-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="e86f2-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="e86f2-120">-ReservationOrder</span></span>
<span data-ttu-id="e86f2-121">Parametr obiektu Pipe dla `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e86f2-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="e86f2-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e86f2-122">-ReservationOrderId</span></span>
<span data-ttu-id="e86f2-123">Identyfikator, `ReservationOrder` który zawiera . `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e86f2-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="e86f2-124">Wymagane.</span><span class="sxs-lookup"><span data-stu-id="e86f2-124">Required.</span></span>

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

### <span data-ttu-id="e86f2-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="e86f2-125">-ReservationOrderPage</span></span>
<span data-ttu-id="e86f2-126">Parametr obiektu Pipe dla `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e86f2-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="e86f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e86f2-127">CommonParameters</span></span>
<span data-ttu-id="e86f2-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e86f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e86f2-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e86f2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e86f2-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e86f2-130">INPUTS</span></span>

### <span data-ttu-id="e86f2-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e86f2-131">System.Guid</span></span>

### <span data-ttu-id="e86f2-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="e86f2-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="e86f2-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="e86f2-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="e86f2-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e86f2-134">OUTPUTS</span></span>

### <span data-ttu-id="e86f2-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="e86f2-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="e86f2-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="e86f2-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e86f2-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e86f2-137">NOTES</span></span>

## <span data-ttu-id="e86f2-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e86f2-138">RELATED LINKS</span></span>

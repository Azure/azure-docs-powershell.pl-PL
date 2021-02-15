---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176435"
---
# <span data-ttu-id="3ca65-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="3ca65-101">Split-AzReservation</span></span>

## <span data-ttu-id="3ca65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca65-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca65-103">Dzielenie. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="3ca65-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="3ca65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3ca65-104">SYNTAX</span></span>

### <span data-ttu-id="3ca65-105">CommandLine (Default)</span><span class="sxs-lookup"><span data-stu-id="3ca65-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca65-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="3ca65-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca65-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3ca65-107">DESCRIPTION</span></span>
<span data-ttu-id="3ca65-108">Podziel wartość a `Reservation` na dwie części przy określonym `Reservation` rozsyłanie ilości.</span><span class="sxs-lookup"><span data-stu-id="3ca65-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="3ca65-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3ca65-109">EXAMPLES</span></span>

### <span data-ttu-id="3ca65-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ca65-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="3ca65-111">Dzielenie określonej `Reservation` wartości na dwie części z odpowiednimi `Reservation` ilościami</span><span class="sxs-lookup"><span data-stu-id="3ca65-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="3ca65-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ca65-112">PARAMETERS</span></span>

### <span data-ttu-id="3ca65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca65-113">-DefaultProfile</span></span>
<span data-ttu-id="3ca65-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca65-115">— Ilość</span><span class="sxs-lookup"><span data-stu-id="3ca65-115">-Quantity</span></span>
<span data-ttu-id="3ca65-116">Liczby całkowite rozdzielane przecinkami dla pola ilości dwóch `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="3ca65-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca65-117">— Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="3ca65-117">-Reservation</span></span>
<span data-ttu-id="3ca65-118">Parametr obiektu Pipe dla `Reservation`</span><span class="sxs-lookup"><span data-stu-id="3ca65-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca65-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="3ca65-119">-ReservationId</span></span>
<span data-ttu-id="3ca65-120">Identyfikator podziału `Reservation`</span><span class="sxs-lookup"><span data-stu-id="3ca65-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca65-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3ca65-121">-ReservationOrderId</span></span>
<span data-ttu-id="3ca65-122">Identyfikator `ReservationOrder` zawierającego `Reservation` użytkownika, który chce podzielić</span><span class="sxs-lookup"><span data-stu-id="3ca65-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca65-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ca65-123">-Confirm</span></span>
<span data-ttu-id="3ca65-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3ca65-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca65-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca65-125">-WhatIf</span></span>
<span data-ttu-id="3ca65-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca65-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ca65-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3ca65-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca65-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca65-128">CommonParameters</span></span>
<span data-ttu-id="3ca65-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca65-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca65-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ca65-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca65-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ca65-131">INPUTS</span></span>

### <span data-ttu-id="3ca65-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="3ca65-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="3ca65-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ca65-133">OUTPUTS</span></span>

### <span data-ttu-id="3ca65-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="3ca65-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="3ca65-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3ca65-135">NOTES</span></span>

## <span data-ttu-id="3ca65-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ca65-136">RELATED LINKS</span></span>

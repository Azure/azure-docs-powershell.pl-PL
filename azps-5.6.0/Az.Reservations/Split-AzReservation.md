---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 9ea53203bc07cca5ca5a8b7909f9fbab558e3c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000170"
---
# <span data-ttu-id="0d8a9-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="0d8a9-101">Split-AzReservation</span></span>

## <span data-ttu-id="0d8a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8a9-103">Dzielenie. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="0d8a9-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="0d8a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0d8a9-104">SYNTAX</span></span>

### <span data-ttu-id="0d8a9-105">CommandLine (Default)</span><span class="sxs-lookup"><span data-stu-id="0d8a9-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d8a9-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="0d8a9-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d8a9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0d8a9-107">DESCRIPTION</span></span>
<span data-ttu-id="0d8a9-108">Podziel wartość a `Reservation` na dwie części przy określonym `Reservation` rozsyłanie ilości.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="0d8a9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0d8a9-109">EXAMPLES</span></span>

### <span data-ttu-id="0d8a9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d8a9-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="0d8a9-111">Dzielenie określonej `Reservation` wartości na dwie części z odpowiednimi `Reservation` ilościami</span><span class="sxs-lookup"><span data-stu-id="0d8a9-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="0d8a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d8a9-112">PARAMETERS</span></span>

### <span data-ttu-id="0d8a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8a9-113">-DefaultProfile</span></span>
<span data-ttu-id="0d8a9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d8a9-115">— Ilość</span><span class="sxs-lookup"><span data-stu-id="0d8a9-115">-Quantity</span></span>
<span data-ttu-id="0d8a9-116">Liczby całkowite rozdzielane przecinkami dla pola ilości dwóch `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="0d8a9-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="0d8a9-117">— Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="0d8a9-117">-Reservation</span></span>
<span data-ttu-id="0d8a9-118">Parametr obiektu Pipe dla `Reservation`</span><span class="sxs-lookup"><span data-stu-id="0d8a9-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="0d8a9-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="0d8a9-119">-ReservationId</span></span>
<span data-ttu-id="0d8a9-120">Identyfikator podziału `Reservation`</span><span class="sxs-lookup"><span data-stu-id="0d8a9-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="0d8a9-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0d8a9-121">-ReservationOrderId</span></span>
<span data-ttu-id="0d8a9-122">Identyfikator `ReservationOrder` zawierającego `Reservation` użytkownika, który chce podzielić</span><span class="sxs-lookup"><span data-stu-id="0d8a9-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="0d8a9-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d8a9-123">-Confirm</span></span>
<span data-ttu-id="0d8a9-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d8a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d8a9-125">-WhatIf</span></span>
<span data-ttu-id="0d8a9-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d8a9-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d8a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8a9-128">CommonParameters</span></span>
<span data-ttu-id="0d8a9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8a9-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d8a9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8a9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d8a9-131">INPUTS</span></span>

### <span data-ttu-id="0d8a9-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="0d8a9-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="0d8a9-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d8a9-133">OUTPUTS</span></span>

### <span data-ttu-id="0d8a9-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="0d8a9-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="0d8a9-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0d8a9-135">NOTES</span></span>

## <span data-ttu-id="0d8a9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d8a9-136">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: 61ae392b3dbe8b73aaabd617b397e953f5caebec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000209"
---
# <span data-ttu-id="9a31c-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="9a31c-101">Merge-AzReservation</span></span>

## <span data-ttu-id="9a31c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a31c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a31c-103">Scala dwa `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="9a31c-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="9a31c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a31c-104">SYNTAX</span></span>

### <span data-ttu-id="9a31c-105">CommandLine (Default)</span><span class="sxs-lookup"><span data-stu-id="9a31c-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a31c-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="9a31c-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a31c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a31c-107">DESCRIPTION</span></span>
<span data-ttu-id="9a31c-108">Scalanie określonych `Reservation` s w `Reservation` nowe.</span><span class="sxs-lookup"><span data-stu-id="9a31c-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="9a31c-109">Te dwie `Reservation` scalone muszą mieć te same właściwości.</span><span class="sxs-lookup"><span data-stu-id="9a31c-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="9a31c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a31c-110">EXAMPLES</span></span>

### <span data-ttu-id="9a31c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a31c-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="9a31c-112">Scalanie dwóch określonych `Reservation` s w jedną `Reservation`</span><span class="sxs-lookup"><span data-stu-id="9a31c-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="9a31c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a31c-113">PARAMETERS</span></span>

### <span data-ttu-id="9a31c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a31c-114">-DefaultProfile</span></span>
<span data-ttu-id="9a31c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a31c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a31c-116">— Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="9a31c-116">-Reservation</span></span>
<span data-ttu-id="9a31c-117">Ciągi dwóch znaków ReservationId do scalenia oddzielone przecinkami</span><span class="sxs-lookup"><span data-stu-id="9a31c-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a31c-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="9a31c-118">-ReservationId</span></span>
<span data-ttu-id="9a31c-119">ReservationOrderId dla `ReservationOrder` tej, która zawiera dwa `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="9a31c-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a31c-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9a31c-120">-ReservationOrderId</span></span>
<span data-ttu-id="9a31c-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="9a31c-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="9a31c-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a31c-122">-Confirm</span></span>
<span data-ttu-id="9a31c-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9a31c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a31c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a31c-124">-WhatIf</span></span>
<span data-ttu-id="9a31c-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a31c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a31c-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9a31c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a31c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a31c-127">CommonParameters</span></span>
<span data-ttu-id="9a31c-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a31c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a31c-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a31c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a31c-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a31c-130">INPUTS</span></span>

### <span data-ttu-id="9a31c-131">Brak</span><span class="sxs-lookup"><span data-stu-id="9a31c-131">None</span></span>

## <span data-ttu-id="9a31c-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a31c-132">OUTPUTS</span></span>

### <span data-ttu-id="9a31c-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="9a31c-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="9a31c-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a31c-134">NOTES</span></span>

## <span data-ttu-id="9a31c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a31c-135">RELATED LINKS</span></span>

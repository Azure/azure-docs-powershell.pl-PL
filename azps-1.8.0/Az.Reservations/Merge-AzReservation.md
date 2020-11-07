---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: 8974a8a0bf8230b630a848e922527bc0b08bdb02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708437"
---
# <span data-ttu-id="dc971-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="dc971-101">Merge-AzReservation</span></span>

## <span data-ttu-id="dc971-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc971-102">SYNOPSIS</span></span>
<span data-ttu-id="dc971-103">Scala dwa `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="dc971-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="dc971-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc971-104">SYNTAX</span></span>

### <span data-ttu-id="dc971-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="dc971-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc971-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="dc971-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc971-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dc971-107">DESCRIPTION</span></span>
<span data-ttu-id="dc971-108">Scal określony `Reservation` s w nowy `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="dc971-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="dc971-109">Oba `Reservation` scalane s muszą mieć te same właściwości.</span><span class="sxs-lookup"><span data-stu-id="dc971-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="dc971-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc971-110">EXAMPLES</span></span>

### <span data-ttu-id="dc971-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc971-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="dc971-112">Scalanie dwóch określonych liter `Reservation` s w jednej `Reservation`</span><span class="sxs-lookup"><span data-stu-id="dc971-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="dc971-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc971-113">PARAMETERS</span></span>

### <span data-ttu-id="dc971-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc971-114">-DefaultProfile</span></span>
<span data-ttu-id="dc971-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc971-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc971-116">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="dc971-116">-Reservation</span></span>
<span data-ttu-id="dc971-117">Ciągi rozdzielane przecinkami dwóch ReservationIds do scalenia</span><span class="sxs-lookup"><span data-stu-id="dc971-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="dc971-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="dc971-118">-ReservationId</span></span>
<span data-ttu-id="dc971-119">ReservationOrderId `ReservationOrder` , który zawiera dwie `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="dc971-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="dc971-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="dc971-120">-ReservationOrderId</span></span>
<span data-ttu-id="dc971-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="dc971-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="dc971-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc971-122">-Confirm</span></span>
<span data-ttu-id="dc971-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc971-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc971-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc971-124">-WhatIf</span></span>
<span data-ttu-id="dc971-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc971-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc971-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc971-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc971-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc971-127">CommonParameters</span></span>
<span data-ttu-id="dc971-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc971-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc971-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc971-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc971-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc971-130">INPUTS</span></span>

### <span data-ttu-id="dc971-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dc971-131">None</span></span>

## <span data-ttu-id="dc971-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc971-132">OUTPUTS</span></span>

### <span data-ttu-id="dc971-133">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="dc971-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="dc971-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc971-134">NOTES</span></span>

## <span data-ttu-id="dc971-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc971-135">RELATED LINKS</span></span>
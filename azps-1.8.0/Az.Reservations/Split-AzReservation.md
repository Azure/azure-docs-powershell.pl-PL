---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 1345978ac502d0c7d576b56f720bd16ca704e062
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708434"
---
# <span data-ttu-id="24f1d-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="24f1d-101">Split-AzReservation</span></span>

## <span data-ttu-id="24f1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="24f1d-103">Podziel a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="24f1d-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="24f1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24f1d-104">SYNTAX</span></span>

### <span data-ttu-id="24f1d-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="24f1d-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f1d-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="24f1d-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f1d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="24f1d-107">DESCRIPTION</span></span>
<span data-ttu-id="24f1d-108">Dzielenie a `Reservation` na dwa `Reservation` s przy użyciu określonego rozkładu ilościowego.</span><span class="sxs-lookup"><span data-stu-id="24f1d-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="24f1d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24f1d-109">EXAMPLES</span></span>

### <span data-ttu-id="24f1d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24f1d-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="24f1d-111">Podziel określoną `Reservation` `Reservation` liczbę z dwóch s na odpowiadające im ilości.</span><span class="sxs-lookup"><span data-stu-id="24f1d-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="24f1d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24f1d-112">PARAMETERS</span></span>

### <span data-ttu-id="24f1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f1d-113">-DefaultProfile</span></span>
<span data-ttu-id="24f1d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24f1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24f1d-115">-Ilość</span><span class="sxs-lookup"><span data-stu-id="24f1d-115">-Quantity</span></span>
<span data-ttu-id="24f1d-116">Liczby całkowite rozdzielane przecinkami dla pola Ilość z dwóch `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="24f1d-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="24f1d-117">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="24f1d-117">-Reservation</span></span>
<span data-ttu-id="24f1d-118">Parametr obiektu potoku `Reservation`</span><span class="sxs-lookup"><span data-stu-id="24f1d-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="24f1d-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="24f1d-119">-ReservationId</span></span>
<span data-ttu-id="24f1d-120">Identyfikator `Reservation` do rozdzielenia</span><span class="sxs-lookup"><span data-stu-id="24f1d-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="24f1d-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="24f1d-121">-ReservationOrderId</span></span>
<span data-ttu-id="24f1d-122">Identyfikator, `ReservationOrder` który zawiera `Reservation` użytkownika, który chce podzielić</span><span class="sxs-lookup"><span data-stu-id="24f1d-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="24f1d-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24f1d-123">-Confirm</span></span>
<span data-ttu-id="24f1d-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f1d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f1d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f1d-125">-WhatIf</span></span>
<span data-ttu-id="24f1d-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f1d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24f1d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24f1d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f1d-128">CommonParameters</span></span>
<span data-ttu-id="24f1d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f1d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f1d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f1d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24f1d-131">INPUTS</span></span>

### <span data-ttu-id="24f1d-132">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="24f1d-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="24f1d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24f1d-133">OUTPUTS</span></span>

### <span data-ttu-id="24f1d-134">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="24f1d-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="24f1d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24f1d-135">NOTES</span></span>

## <span data-ttu-id="24f1d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24f1d-136">RELATED LINKS</span></span>
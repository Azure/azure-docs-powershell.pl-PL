---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: bc1fba5c7fa7e01a3c2461907a214809e175f3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526066"
---
# <span data-ttu-id="01125-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="01125-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="01125-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01125-102">SYNOPSIS</span></span>
<span data-ttu-id="01125-103">Podziel a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="01125-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01125-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01125-104">SYNTAX</span></span>

### <span data-ttu-id="01125-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="01125-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01125-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="01125-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Int32[]> -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01125-107">Opis</span><span class="sxs-lookup"><span data-stu-id="01125-107">DESCRIPTION</span></span>
<span data-ttu-id="01125-108">Dzielenie a `Reservation` na dwa `Reservation` s przy użyciu określonego rozkładu ilościowego.</span><span class="sxs-lookup"><span data-stu-id="01125-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="01125-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01125-109">EXAMPLES</span></span>

### <span data-ttu-id="01125-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01125-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="01125-111">Podziel określoną `Reservation` `Reservation` liczbę z dwóch s na odpowiadające im ilości.</span><span class="sxs-lookup"><span data-stu-id="01125-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="01125-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01125-112">PARAMETERS</span></span>

### <span data-ttu-id="01125-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01125-113">-DefaultProfile</span></span>
<span data-ttu-id="01125-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01125-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01125-115">-Ilość</span><span class="sxs-lookup"><span data-stu-id="01125-115">-Quantity</span></span>
<span data-ttu-id="01125-116">Liczby całkowite rozdzielane przecinkami dla pola Ilość z dwóch `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="01125-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="01125-117">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="01125-117">-Reservation</span></span>
<span data-ttu-id="01125-118">Parametr obiektu potoku `Reservation`</span><span class="sxs-lookup"><span data-stu-id="01125-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="01125-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="01125-119">-ReservationId</span></span>
<span data-ttu-id="01125-120">Identyfikator `Reservation` do rozdzielenia</span><span class="sxs-lookup"><span data-stu-id="01125-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="01125-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="01125-121">-ReservationOrderId</span></span>
<span data-ttu-id="01125-122">Identyfikator, `ReservationOrder` który zawiera `Reservation` użytkownika, który chce podzielić</span><span class="sxs-lookup"><span data-stu-id="01125-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="01125-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01125-123">-Confirm</span></span>
<span data-ttu-id="01125-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01125-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01125-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01125-125">-WhatIf</span></span>
<span data-ttu-id="01125-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01125-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01125-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01125-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01125-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01125-128">CommonParameters</span></span>
<span data-ttu-id="01125-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01125-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01125-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01125-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01125-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01125-131">INPUTS</span></span>

### <span data-ttu-id="01125-132">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="01125-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="01125-133">Parametry: rezerwacja (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01125-133">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="01125-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01125-134">OUTPUTS</span></span>

### <span data-ttu-id="01125-135">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="01125-135">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="01125-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01125-136">NOTES</span></span>

## <span data-ttu-id="01125-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01125-137">RELATED LINKS</span></span>

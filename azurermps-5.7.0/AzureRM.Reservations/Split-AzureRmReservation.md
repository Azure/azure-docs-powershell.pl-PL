---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544152"
---
# <span data-ttu-id="3a144-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="3a144-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="3a144-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a144-102">SYNOPSIS</span></span>
<span data-ttu-id="3a144-103">Podziel a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="3a144-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a144-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a144-104">SYNTAX</span></span>

### <span data-ttu-id="3a144-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3a144-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a144-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="3a144-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a144-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3a144-107">DESCRIPTION</span></span>
<span data-ttu-id="3a144-108">Dzielenie a `Reservation` na dwa `Reservation` s przy użyciu określonego rozkładu ilościowego.</span><span class="sxs-lookup"><span data-stu-id="3a144-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="3a144-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a144-109">EXAMPLES</span></span>

### <span data-ttu-id="3a144-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a144-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="3a144-111">Podziel określoną `Reservation` `Reservation` liczbę z dwóch s na odpowiadające im ilości.</span><span class="sxs-lookup"><span data-stu-id="3a144-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="3a144-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a144-112">PARAMETERS</span></span>

### <span data-ttu-id="3a144-113">-Ilość</span><span class="sxs-lookup"><span data-stu-id="3a144-113">-Quantity</span></span>
<span data-ttu-id="3a144-114">Liczby całkowite rozdzielane przecinkami dla pola Ilość z dwóch `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="3a144-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a144-115">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="3a144-115">-Reservation</span></span>
<span data-ttu-id="3a144-116">Parametr obiektu potoku `Reservation`</span><span class="sxs-lookup"><span data-stu-id="3a144-116">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a144-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="3a144-117">-ReservationId</span></span>
<span data-ttu-id="3a144-118">Identyfikator `Reservation` do rozdzielenia</span><span class="sxs-lookup"><span data-stu-id="3a144-118">Id of the `Reservation` to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a144-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3a144-119">-ReservationOrderId</span></span>
<span data-ttu-id="3a144-120">Identyfikator, `ReservationOrder` który zawiera `Reservation` użytkownika, który chce podzielić</span><span class="sxs-lookup"><span data-stu-id="3a144-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a144-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a144-121">-Confirm</span></span>
<span data-ttu-id="3a144-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a144-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a144-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a144-123">-WhatIf</span></span>
<span data-ttu-id="3a144-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a144-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a144-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a144-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a144-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a144-126">CommonParameters</span></span>
<span data-ttu-id="3a144-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a144-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a144-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a144-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a144-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a144-129">INPUTS</span></span>

### <span data-ttu-id="3a144-130">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="3a144-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="3a144-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a144-131">OUTPUTS</span></span>

### <span data-ttu-id="3a144-132">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. rezerwacje. modele. PSReservation, Microsoft. Azure. Commands. rezerwacje, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3a144-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3a144-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a144-133">NOTES</span></span>

## <span data-ttu-id="3a144-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a144-134">RELATED LINKS</span></span>


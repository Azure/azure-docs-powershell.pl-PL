---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544151"
---
# <span data-ttu-id="9d54b-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="9d54b-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="9d54b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d54b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d54b-103">Scala dwa `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="9d54b-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d54b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d54b-104">SYNTAX</span></span>

### <span data-ttu-id="9d54b-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9d54b-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d54b-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="9d54b-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d54b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9d54b-107">DESCRIPTION</span></span>
<span data-ttu-id="9d54b-108">Scal określony `Reservation` s w nowy `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="9d54b-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="9d54b-109">Oba `Reservation` scalane s muszą mieć te same właściwości.</span><span class="sxs-lookup"><span data-stu-id="9d54b-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="9d54b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d54b-110">EXAMPLES</span></span>

### <span data-ttu-id="9d54b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d54b-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="9d54b-112">Scalanie dwóch określonych liter `Reservation` s w jednej `Reservation`</span><span class="sxs-lookup"><span data-stu-id="9d54b-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="9d54b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d54b-113">PARAMETERS</span></span>

### <span data-ttu-id="9d54b-114">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="9d54b-114">-Reservation</span></span>
<span data-ttu-id="9d54b-115">Ciągi rozdzielane przecinkami dwóch ReservationIds do scalenia</span><span class="sxs-lookup"><span data-stu-id="9d54b-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d54b-116">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="9d54b-116">-ReservationId</span></span>
<span data-ttu-id="9d54b-117">ReservationOrderId `ReservationOrder` , który zawiera dwie `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="9d54b-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d54b-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9d54b-118">-ReservationOrderId</span></span>
<span data-ttu-id="9d54b-119">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="9d54b-119">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="9d54b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d54b-120">-Confirm</span></span>
<span data-ttu-id="9d54b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d54b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d54b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d54b-122">-WhatIf</span></span>
<span data-ttu-id="9d54b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d54b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d54b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d54b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d54b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d54b-125">CommonParameters</span></span>
<span data-ttu-id="9d54b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d54b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d54b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d54b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d54b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d54b-128">INPUTS</span></span>

### <span data-ttu-id="9d54b-129">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="9d54b-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="9d54b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d54b-130">OUTPUTS</span></span>

### <span data-ttu-id="9d54b-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. rezerwacje. modele. PSReservation, Microsoft. Azure. Commands. rezerwacje, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9d54b-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9d54b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d54b-132">NOTES</span></span>

## <span data-ttu-id="9d54b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d54b-133">RELATED LINKS</span></span>


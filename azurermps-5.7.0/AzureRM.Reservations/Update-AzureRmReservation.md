---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544140"
---
# <span data-ttu-id="c4e65-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="c4e65-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="c4e65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4e65-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e65-103">Aktualizacja a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c4e65-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4e65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4e65-104">SYNTAX</span></span>

### <span data-ttu-id="c4e65-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c4e65-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e65-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="c4e65-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4e65-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c4e65-107">DESCRIPTION</span></span>
<span data-ttu-id="c4e65-108">Aktualizuje zastosowane zakresy `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c4e65-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="c4e65-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4e65-109">EXAMPLES</span></span>

### <span data-ttu-id="c4e65-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c4e65-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="c4e65-111">Aktualizuje AppliedScopeType określonej rezerwacji do jednego</span><span class="sxs-lookup"><span data-stu-id="c4e65-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="c4e65-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c4e65-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="c4e65-113">Aktualizuje AppliedScopeType określonej rezerwacji do współdzielonej</span><span class="sxs-lookup"><span data-stu-id="c4e65-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="c4e65-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4e65-114">PARAMETERS</span></span>

### <span data-ttu-id="c4e65-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="c4e65-115">-AppliedScope</span></span>
<span data-ttu-id="c4e65-116">Identyfikator subskrypcji `Reservation` do zastosowania</span><span class="sxs-lookup"><span data-stu-id="c4e65-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e65-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="c4e65-117">-AppliedScopeType</span></span>
<span data-ttu-id="c4e65-118">Typ `Reservation` do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="c4e65-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e65-119">-DefaultProfile</span></span>
<span data-ttu-id="c4e65-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4e65-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e65-121">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="c4e65-121">-Reservation</span></span>
<span data-ttu-id="c4e65-122">Parametr obiektu potoku `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c4e65-122">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="c4e65-123">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="c4e65-123">-ReservationId</span></span>
<span data-ttu-id="c4e65-124">Identyfikator `Reservation` aktualizacji</span><span class="sxs-lookup"><span data-stu-id="c4e65-124">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="c4e65-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c4e65-125">-ReservationOrderId</span></span>
<span data-ttu-id="c4e65-126">Identyfikator `ReservationOrder` aktualizacji</span><span class="sxs-lookup"><span data-stu-id="c4e65-126">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="c4e65-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4e65-127">-Confirm</span></span>
<span data-ttu-id="c4e65-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4e65-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e65-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e65-129">-WhatIf</span></span>
<span data-ttu-id="c4e65-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4e65-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4e65-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4e65-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e65-132">CommonParameters</span></span>
<span data-ttu-id="c4e65-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e65-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e65-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e65-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4e65-135">INPUTS</span></span>

### <span data-ttu-id="c4e65-136">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c4e65-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c4e65-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4e65-137">OUTPUTS</span></span>

### <span data-ttu-id="c4e65-138">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c4e65-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c4e65-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4e65-139">NOTES</span></span>

## <span data-ttu-id="c4e65-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4e65-140">RELATED LINKS</span></span>


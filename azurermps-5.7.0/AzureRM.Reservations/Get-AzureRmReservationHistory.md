---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549587"
---
# <span data-ttu-id="08ab7-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="08ab7-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="08ab7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="08ab7-103">Uzyskaj `Reservation` historię poprawek.</span><span class="sxs-lookup"><span data-stu-id="08ab7-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08ab7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08ab7-104">SYNTAX</span></span>

### <span data-ttu-id="08ab7-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="08ab7-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="08ab7-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="08ab7-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="08ab7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="08ab7-107">DESCRIPTION</span></span>
<span data-ttu-id="08ab7-108">Lista wszystkich poprawek `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="08ab7-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="08ab7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08ab7-109">EXAMPLES</span></span>

### <span data-ttu-id="08ab7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="08ab7-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="08ab7-111">Pobieranie historii poprawek dla konkretnej rezerwacji</span><span class="sxs-lookup"><span data-stu-id="08ab7-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="08ab7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08ab7-112">PARAMETERS</span></span>

### <span data-ttu-id="08ab7-113">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="08ab7-113">-Reservation</span></span>
<span data-ttu-id="08ab7-114">Parametr obiektu potoku dla `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="08ab7-114">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="08ab7-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="08ab7-115">-ReservationId</span></span>
<span data-ttu-id="08ab7-116">ReservationId, z `Reservation` której ma zostać wyświetlona historia</span><span class="sxs-lookup"><span data-stu-id="08ab7-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ab7-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="08ab7-117">-ReservationOrderId</span></span>
<span data-ttu-id="08ab7-118">ReservationOrderId, `ReservationOrder` który zawiera `Reservation`</span><span class="sxs-lookup"><span data-stu-id="08ab7-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ab7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ab7-119">CommonParameters</span></span>
<span data-ttu-id="08ab7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ab7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ab7-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ab7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ab7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08ab7-122">INPUTS</span></span>

### <span data-ttu-id="08ab7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="08ab7-123">System.String</span></span>
<span data-ttu-id="08ab7-124">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="08ab7-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="08ab7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08ab7-125">OUTPUTS</span></span>

### <span data-ttu-id="08ab7-126">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="08ab7-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="08ab7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08ab7-127">NOTES</span></span>

## <span data-ttu-id="08ab7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08ab7-128">RELATED LINKS</span></span>


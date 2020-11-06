---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554259"
---
# <span data-ttu-id="a4a98-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="a4a98-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="a4a98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4a98-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a98-103">Uzyskaj `Reservation` historię poprawek.</span><span class="sxs-lookup"><span data-stu-id="a4a98-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4a98-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4a98-104">SYNTAX</span></span>

### <span data-ttu-id="a4a98-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a4a98-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4a98-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="a4a98-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a98-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a4a98-107">DESCRIPTION</span></span>
<span data-ttu-id="a4a98-108">Lista wszystkich poprawek `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="a4a98-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="a4a98-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4a98-109">EXAMPLES</span></span>

### <span data-ttu-id="a4a98-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4a98-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="a4a98-111">Pobieranie historii poprawek dla konkretnej rezerwacji</span><span class="sxs-lookup"><span data-stu-id="a4a98-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="a4a98-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4a98-112">PARAMETERS</span></span>

### <span data-ttu-id="a4a98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a98-113">-DefaultProfile</span></span>
<span data-ttu-id="a4a98-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a98-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a98-115">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="a4a98-115">-Reservation</span></span>
<span data-ttu-id="a4a98-116">Parametr obiektu potoku dla `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="a4a98-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="a4a98-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a4a98-117">-ReservationId</span></span>
<span data-ttu-id="a4a98-118">ReservationId, z `Reservation` której ma zostać wyświetlona historia</span><span class="sxs-lookup"><span data-stu-id="a4a98-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a98-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a4a98-119">-ReservationOrderId</span></span>
<span data-ttu-id="a4a98-120">ReservationOrderId, `ReservationOrder` który zawiera `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a4a98-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a98-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a98-121">CommonParameters</span></span>
<span data-ttu-id="a4a98-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a98-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a98-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a98-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a98-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4a98-124">INPUTS</span></span>

### <span data-ttu-id="a4a98-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a4a98-125">System.Guid</span></span>

### <span data-ttu-id="a4a98-126">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="a4a98-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="a4a98-127">Parametry: rezerwacja (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4a98-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="a4a98-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4a98-128">OUTPUTS</span></span>

### <span data-ttu-id="a4a98-129">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="a4a98-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="a4a98-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4a98-130">NOTES</span></span>

## <span data-ttu-id="a4a98-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4a98-131">RELATED LINKS</span></span>

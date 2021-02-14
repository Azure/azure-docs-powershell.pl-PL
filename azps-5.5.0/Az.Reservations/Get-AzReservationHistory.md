---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183738"
---
# <span data-ttu-id="96050-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="96050-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="96050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96050-102">SYNOPSIS</span></span>
<span data-ttu-id="96050-103">Pobierz `Reservation` historię poprawek.</span><span class="sxs-lookup"><span data-stu-id="96050-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="96050-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="96050-104">SYNTAX</span></span>

### <span data-ttu-id="96050-105">CommandLine (Default)</span><span class="sxs-lookup"><span data-stu-id="96050-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96050-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="96050-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96050-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="96050-107">DESCRIPTION</span></span>
<span data-ttu-id="96050-108">Lista wszystkich poprawek dla `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="96050-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="96050-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="96050-109">EXAMPLES</span></span>

### <span data-ttu-id="96050-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96050-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="96050-111">Uzyskiwanie historii poprawek dla danego rezerwacji</span><span class="sxs-lookup"><span data-stu-id="96050-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="96050-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96050-112">PARAMETERS</span></span>

### <span data-ttu-id="96050-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96050-113">-DefaultProfile</span></span>
<span data-ttu-id="96050-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="96050-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96050-115">— Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="96050-115">-Reservation</span></span>
<span data-ttu-id="96050-116">Parametr obiektu pipety dla `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="96050-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="96050-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="96050-117">-ReservationId</span></span>
<span data-ttu-id="96050-118">ReservationId , `Reservation` którego historia ma być wyświetlana</span><span class="sxs-lookup"><span data-stu-id="96050-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="96050-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="96050-119">-ReservationOrderId</span></span>
<span data-ttu-id="96050-120">ReservationOrderId dla `ReservationOrder` zawierającego `Reservation`</span><span class="sxs-lookup"><span data-stu-id="96050-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="96050-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96050-121">CommonParameters</span></span>
<span data-ttu-id="96050-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96050-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96050-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96050-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96050-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96050-124">INPUTS</span></span>

### <span data-ttu-id="96050-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="96050-125">System.Guid</span></span>

### <span data-ttu-id="96050-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="96050-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="96050-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96050-127">OUTPUTS</span></span>

### <span data-ttu-id="96050-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="96050-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="96050-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="96050-129">NOTES</span></span>

## <span data-ttu-id="96050-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96050-130">RELATED LINKS</span></span>

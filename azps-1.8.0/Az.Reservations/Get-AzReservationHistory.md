---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cf68c40a13247d1101f6d25abac92f01ae1a0053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708447"
---
# <span data-ttu-id="8fd81-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="8fd81-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="8fd81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8fd81-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd81-103">Uzyskaj `Reservation` historię poprawek.</span><span class="sxs-lookup"><span data-stu-id="8fd81-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="8fd81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8fd81-104">SYNTAX</span></span>

### <span data-ttu-id="8fd81-105">Wiersz polecenia (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8fd81-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fd81-106">Potokobject</span><span class="sxs-lookup"><span data-stu-id="8fd81-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fd81-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8fd81-107">DESCRIPTION</span></span>
<span data-ttu-id="8fd81-108">Lista wszystkich poprawek `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="8fd81-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="8fd81-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8fd81-109">EXAMPLES</span></span>

### <span data-ttu-id="8fd81-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8fd81-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="8fd81-111">Pobieranie historii poprawek dla konkretnej rezerwacji</span><span class="sxs-lookup"><span data-stu-id="8fd81-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="8fd81-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8fd81-112">PARAMETERS</span></span>

### <span data-ttu-id="8fd81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd81-113">-DefaultProfile</span></span>
<span data-ttu-id="8fd81-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fd81-115">-Rezerwacja</span><span class="sxs-lookup"><span data-stu-id="8fd81-115">-Reservation</span></span>
<span data-ttu-id="8fd81-116">Parametr obiektu potoku dla `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="8fd81-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="8fd81-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="8fd81-117">-ReservationId</span></span>
<span data-ttu-id="8fd81-118">ReservationId, z `Reservation` której ma zostać wyświetlona historia</span><span class="sxs-lookup"><span data-stu-id="8fd81-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="8fd81-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8fd81-119">-ReservationOrderId</span></span>
<span data-ttu-id="8fd81-120">ReservationOrderId, `ReservationOrder` który zawiera `Reservation`</span><span class="sxs-lookup"><span data-stu-id="8fd81-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="8fd81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd81-121">CommonParameters</span></span>
<span data-ttu-id="8fd81-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd81-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd81-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd81-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fd81-124">INPUTS</span></span>

### <span data-ttu-id="8fd81-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8fd81-125">System.Guid</span></span>

### <span data-ttu-id="8fd81-126">Microsoft. Azure. Commands. rezerwacje. modele. PSReservation</span><span class="sxs-lookup"><span data-stu-id="8fd81-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="8fd81-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8fd81-127">OUTPUTS</span></span>

### <span data-ttu-id="8fd81-128">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="8fd81-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="8fd81-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8fd81-129">NOTES</span></span>

## <span data-ttu-id="8fd81-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fd81-130">RELATED LINKS</span></span>
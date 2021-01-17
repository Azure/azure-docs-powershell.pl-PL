---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370078"
---
# <span data-ttu-id="970ad-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="970ad-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="970ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="970ad-102">SYNOPSIS</span></span>
<span data-ttu-id="970ad-103">Pobierz listę odpowiednich `ReservationOrder` identyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="970ad-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="970ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="970ad-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="970ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="970ad-105">DESCRIPTION</span></span>
<span data-ttu-id="970ad-106">Uzyskaj identyfikatory odpowiednich `ReservationOrder` s, które można zastosować do tego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="970ad-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="970ad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="970ad-107">EXAMPLES</span></span>

### <span data-ttu-id="970ad-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="970ad-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="970ad-109">Zastosowana `ReservationOrder` do subskrypcji domyślnej</span><span class="sxs-lookup"><span data-stu-id="970ad-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="970ad-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="970ad-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="970ad-111">Zastosowana `ReservationOrder` do określonego abonamentu</span><span class="sxs-lookup"><span data-stu-id="970ad-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="970ad-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="970ad-112">PARAMETERS</span></span>

### <span data-ttu-id="970ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="970ad-113">-DefaultProfile</span></span>
<span data-ttu-id="970ad-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="970ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="970ad-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="970ad-115">-SubscriptionId</span></span>
<span data-ttu-id="970ad-116">Identyfikator subskrypcji, aby uzyskać zastosowany `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="970ad-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="970ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="970ad-117">CommonParameters</span></span>
<span data-ttu-id="970ad-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="970ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="970ad-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="970ad-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="970ad-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="970ad-120">INPUTS</span></span>

### <span data-ttu-id="970ad-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="970ad-121">None</span></span>

## <span data-ttu-id="970ad-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="970ad-122">OUTPUTS</span></span>

### <span data-ttu-id="970ad-123">Microsoft. Azure. Management. rezerwacje. modele. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="970ad-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="970ad-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="970ad-124">NOTES</span></span>

## <span data-ttu-id="970ad-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="970ad-125">RELATED LINKS</span></span>

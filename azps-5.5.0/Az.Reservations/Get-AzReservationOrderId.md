---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183731"
---
# <span data-ttu-id="27259-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="27259-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="27259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27259-102">SYNOPSIS</span></span>
<span data-ttu-id="27259-103">Uzyskaj listę odpowiednich `ReservationOrder` identyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="27259-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="27259-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27259-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27259-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="27259-105">DESCRIPTION</span></span>
<span data-ttu-id="27259-106">Uzyskaj identyfikatory odpowiednich `ReservationOrder` usług, które można zastosować do tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="27259-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="27259-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27259-107">EXAMPLES</span></span>

### <span data-ttu-id="27259-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27259-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="27259-109">Pobierz `ReservationOrder` wniosek o subskrypcję domyślną</span><span class="sxs-lookup"><span data-stu-id="27259-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="27259-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="27259-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="27259-111">Uzyskiwanie zastosowania `ReservationOrder` do określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="27259-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="27259-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27259-112">PARAMETERS</span></span>

### <span data-ttu-id="27259-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27259-113">-DefaultProfile</span></span>
<span data-ttu-id="27259-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="27259-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27259-115">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27259-115">-SubscriptionId</span></span>
<span data-ttu-id="27259-116">Identyfikator subskrypcji w celu uzyskania `ReservationOrder` zastosowanych</span><span class="sxs-lookup"><span data-stu-id="27259-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="27259-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27259-117">CommonParameters</span></span>
<span data-ttu-id="27259-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27259-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27259-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27259-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27259-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27259-120">INPUTS</span></span>

### <span data-ttu-id="27259-121">Brak</span><span class="sxs-lookup"><span data-stu-id="27259-121">None</span></span>

## <span data-ttu-id="27259-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27259-122">OUTPUTS</span></span>

### <span data-ttu-id="27259-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="27259-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="27259-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27259-124">NOTES</span></span>

## <span data-ttu-id="27259-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27259-125">RELATED LINKS</span></span>

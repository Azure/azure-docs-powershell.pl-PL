---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 1878237544cc1b44b5e47814f455638c168e2412
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000273"
---
# <span data-ttu-id="405d6-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="405d6-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="405d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="405d6-102">SYNOPSIS</span></span>
<span data-ttu-id="405d6-103">Pobierz `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="405d6-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="405d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="405d6-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="405d6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="405d6-105">DESCRIPTION</span></span>
<span data-ttu-id="405d6-106">Lista wszystkich `ReservationOrder` s, do których użytkownik ma dostęp w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="405d6-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="405d6-107">Jeśli parametr ReservationOrderId jest ustawiony, pobierz ten konkretny parametr ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="405d6-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="405d6-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="405d6-108">EXAMPLES</span></span>

### <span data-ttu-id="405d6-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="405d6-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="405d6-110">Lista wszystkich `ReservationOrder` elementów, do których użytkownik ma dostęp w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="405d6-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="405d6-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="405d6-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="405d6-112">Uzyskiwanie `ReservationOrder` z określoną wartością ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="405d6-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="405d6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="405d6-113">PARAMETERS</span></span>

### <span data-ttu-id="405d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="405d6-114">-DefaultProfile</span></span>
<span data-ttu-id="405d6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="405d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="405d6-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="405d6-116">-ReservationOrderId</span></span>
<span data-ttu-id="405d6-117">Identyfikator konkretnego zamówienia rezerwacji, który ma zostać wyświetlony przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="405d6-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="405d6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="405d6-118">CommonParameters</span></span>
<span data-ttu-id="405d6-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="405d6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="405d6-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="405d6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="405d6-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="405d6-121">INPUTS</span></span>

### <span data-ttu-id="405d6-122">Brak</span><span class="sxs-lookup"><span data-stu-id="405d6-122">None</span></span>

## <span data-ttu-id="405d6-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="405d6-123">OUTPUTS</span></span>

### <span data-ttu-id="405d6-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="405d6-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="405d6-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="405d6-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="405d6-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="405d6-126">NOTES</span></span>

## <span data-ttu-id="405d6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="405d6-127">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201915"
---
# <span data-ttu-id="3ec7f-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="3ec7f-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="3ec7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ec7f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec7f-103">Pobierz `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="3ec7f-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="3ec7f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3ec7f-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ec7f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3ec7f-105">DESCRIPTION</span></span>
<span data-ttu-id="3ec7f-106">Lista wszystkich `ReservationOrder` s, do których użytkownik ma dostęp w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="3ec7f-107">Jeśli parametr ReservationOrderId jest ustawiony, pobierz ten konkretny parametr ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="3ec7f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3ec7f-108">EXAMPLES</span></span>

### <span data-ttu-id="3ec7f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ec7f-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="3ec7f-110">Lista wszystkich `ReservationOrder` elementów, do których użytkownik ma dostęp w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="3ec7f-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="3ec7f-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3ec7f-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="3ec7f-112">Uzyskiwanie `ReservationOrder` z określoną wartością ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3ec7f-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="3ec7f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ec7f-113">PARAMETERS</span></span>

### <span data-ttu-id="3ec7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec7f-114">-DefaultProfile</span></span>
<span data-ttu-id="3ec7f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ec7f-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3ec7f-116">-ReservationOrderId</span></span>
<span data-ttu-id="3ec7f-117">Identyfikator konkretnego zamówienia rezerwacji, który ma zostać wyświetlony przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="3ec7f-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="3ec7f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec7f-118">CommonParameters</span></span>
<span data-ttu-id="3ec7f-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec7f-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ec7f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec7f-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ec7f-121">INPUTS</span></span>

### <span data-ttu-id="3ec7f-122">Brak</span><span class="sxs-lookup"><span data-stu-id="3ec7f-122">None</span></span>

## <span data-ttu-id="3ec7f-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ec7f-123">OUTPUTS</span></span>

### <span data-ttu-id="3ec7f-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="3ec7f-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="3ec7f-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="3ec7f-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="3ec7f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3ec7f-126">NOTES</span></span>

## <span data-ttu-id="3ec7f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ec7f-127">RELATED LINKS</span></span>

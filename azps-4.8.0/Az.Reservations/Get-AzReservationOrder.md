---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223650"
---
# <span data-ttu-id="0a7a8-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="0a7a8-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="0a7a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a7a8-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7a8-103">Pobierz `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="0a7a8-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="0a7a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a7a8-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a7a8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a7a8-105">DESCRIPTION</span></span>
<span data-ttu-id="0a7a8-106">Lista wszystkich `ReservationOrder` osób, do których użytkownik ma dostęp w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="0a7a8-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="0a7a8-107">Jeśli parametr ReservationOrderId jest ustawiony, Pobierz określone ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="0a7a8-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="0a7a8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a7a8-108">EXAMPLES</span></span>

### <span data-ttu-id="0a7a8-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0a7a8-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="0a7a8-110">Lista wszystkich `ReservationOrder` użytkowników, do których użytkownik ma dostęp w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="0a7a8-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="0a7a8-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0a7a8-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="0a7a8-112">Zapoznaj `ReservationOrder` się z określoną ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0a7a8-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="0a7a8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a7a8-113">PARAMETERS</span></span>

### <span data-ttu-id="0a7a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7a8-114">-DefaultProfile</span></span>
<span data-ttu-id="0a7a8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a7a8-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0a7a8-116">-ReservationOrderId</span></span>
<span data-ttu-id="0a7a8-117">Identyfikator konkretnego ReservationOrder, który użytkownik chce zobaczyć</span><span class="sxs-lookup"><span data-stu-id="0a7a8-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="0a7a8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7a8-118">CommonParameters</span></span>
<span data-ttu-id="0a7a8-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a7a8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7a8-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a7a8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7a8-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a7a8-121">INPUTS</span></span>

### <span data-ttu-id="0a7a8-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0a7a8-122">None</span></span>

## <span data-ttu-id="0a7a8-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a7a8-123">OUTPUTS</span></span>

### <span data-ttu-id="0a7a8-124">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="0a7a8-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="0a7a8-125">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="0a7a8-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="0a7a8-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a7a8-126">NOTES</span></span>

## <span data-ttu-id="0a7a8-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a7a8-127">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 3db5c7bf9665498236c3d0dacf05107926ed45eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708445"
---
# <span data-ttu-id="cc5e7-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="cc5e7-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="cc5e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5e7-103">Pobierz `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="cc5e7-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="cc5e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc5e7-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc5e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc5e7-105">DESCRIPTION</span></span>
<span data-ttu-id="cc5e7-106">Lista wszystkich `ReservationOrder` osób, do których użytkownik ma dostęp w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="cc5e7-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="cc5e7-107">Jeśli parametr ReservationOrderId jest ustawiony, Pobierz określone ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="cc5e7-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="cc5e7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc5e7-108">EXAMPLES</span></span>

### <span data-ttu-id="cc5e7-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc5e7-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="cc5e7-110">Lista wszystkich `ReservationOrder` użytkowników, do których użytkownik ma dostęp w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="cc5e7-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="cc5e7-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cc5e7-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="cc5e7-112">Zapoznaj `ReservationOrder` się z określoną ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="cc5e7-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="cc5e7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc5e7-113">PARAMETERS</span></span>

### <span data-ttu-id="cc5e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5e7-114">-DefaultProfile</span></span>
<span data-ttu-id="cc5e7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc5e7-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="cc5e7-116">-ReservationOrderId</span></span>
<span data-ttu-id="cc5e7-117">Identyfikator konkretnego ReservationOrder, który użytkownik chce zobaczyć</span><span class="sxs-lookup"><span data-stu-id="cc5e7-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="cc5e7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5e7-118">CommonParameters</span></span>
<span data-ttu-id="cc5e7-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc5e7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5e7-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc5e7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5e7-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc5e7-121">INPUTS</span></span>

### <span data-ttu-id="cc5e7-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cc5e7-122">None</span></span>

## <span data-ttu-id="cc5e7-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc5e7-123">OUTPUTS</span></span>

### <span data-ttu-id="cc5e7-124">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="cc5e7-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="cc5e7-125">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="cc5e7-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="cc5e7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc5e7-126">NOTES</span></span>

## <span data-ttu-id="cc5e7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc5e7-127">RELATED LINKS</span></span>

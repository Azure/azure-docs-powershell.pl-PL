---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544148"
---
# <span data-ttu-id="9d411-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9d411-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="9d411-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d411-102">SYNOPSIS</span></span>
<span data-ttu-id="9d411-103">Pobierz listę odpowiednich `ReservationOrder` identyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="9d411-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d411-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d411-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="9d411-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d411-105">DESCRIPTION</span></span>
<span data-ttu-id="9d411-106">Uzyskaj identyfikatory odpowiednich `ReservationOrder` s, które można zastosować do tego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="9d411-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="9d411-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d411-107">EXAMPLES</span></span>

### <span data-ttu-id="9d411-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d411-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="9d411-109">Zastosowana `ReservationOrder` do subskrypcji domyślnej</span><span class="sxs-lookup"><span data-stu-id="9d411-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="9d411-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9d411-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="9d411-111">Zastosowana `ReservationOrder` do określonego abonamentu</span><span class="sxs-lookup"><span data-stu-id="9d411-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="9d411-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d411-112">PARAMETERS</span></span>

### <span data-ttu-id="9d411-113">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9d411-113">-SubscriptionId</span></span>
<span data-ttu-id="9d411-114">Identyfikator subskrypcji, aby uzyskać zastosowany `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="9d411-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d411-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d411-115">CommonParameters</span></span>
<span data-ttu-id="9d411-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d411-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d411-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d411-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d411-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d411-118">INPUTS</span></span>

### <span data-ttu-id="9d411-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9d411-119">None</span></span>

## <span data-ttu-id="9d411-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d411-120">OUTPUTS</span></span>

### <span data-ttu-id="9d411-121">Microsoft. Azure. Commands. rezerwacje. modele. PSAppliedReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9d411-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="9d411-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d411-122">NOTES</span></span>

## <span data-ttu-id="9d411-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d411-123">RELATED LINKS</span></span>


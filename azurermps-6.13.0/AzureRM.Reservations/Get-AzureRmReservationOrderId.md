---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: 1e60ca2ce1a845fa460e14a4e99b921fa4c085ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541535"
---
# <span data-ttu-id="03ad1-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="03ad1-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="03ad1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="03ad1-103">Pobierz listę odpowiednich `ReservationOrder` identyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="03ad1-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03ad1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03ad1-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03ad1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03ad1-105">DESCRIPTION</span></span>
<span data-ttu-id="03ad1-106">Uzyskaj identyfikatory odpowiednich `ReservationOrder` s, które można zastosować do tego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="03ad1-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="03ad1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03ad1-107">EXAMPLES</span></span>

### <span data-ttu-id="03ad1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03ad1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="03ad1-109">Zastosowana `ReservationOrder` do subskrypcji domyślnej</span><span class="sxs-lookup"><span data-stu-id="03ad1-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="03ad1-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="03ad1-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="03ad1-111">Zastosowana `ReservationOrder` do określonego abonamentu</span><span class="sxs-lookup"><span data-stu-id="03ad1-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="03ad1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03ad1-112">PARAMETERS</span></span>

### <span data-ttu-id="03ad1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ad1-113">-DefaultProfile</span></span>
<span data-ttu-id="03ad1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03ad1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03ad1-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="03ad1-115">-SubscriptionId</span></span>
<span data-ttu-id="03ad1-116">Identyfikator subskrypcji, aby uzyskać zastosowany `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="03ad1-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="03ad1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ad1-117">CommonParameters</span></span>
<span data-ttu-id="03ad1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ad1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ad1-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ad1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ad1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03ad1-120">INPUTS</span></span>

### <span data-ttu-id="03ad1-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="03ad1-121">None</span></span>

## <span data-ttu-id="03ad1-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03ad1-122">OUTPUTS</span></span>

### <span data-ttu-id="03ad1-123">Microsoft. Azure. Management. rezerwacje. modele. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="03ad1-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="03ad1-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03ad1-124">NOTES</span></span>

## <span data-ttu-id="03ad1-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03ad1-125">RELATED LINKS</span></span>

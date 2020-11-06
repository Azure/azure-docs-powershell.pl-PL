---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544155"
---
# <span data-ttu-id="8de95-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="8de95-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="8de95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8de95-102">SYNOPSIS</span></span>
<span data-ttu-id="8de95-103">Pobierz `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8de95-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8de95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8de95-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## <span data-ttu-id="8de95-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8de95-105">DESCRIPTION</span></span>
<span data-ttu-id="8de95-106">Lista wszystkich `ReservationOrder` osób, do których użytkownik ma dostęp w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="8de95-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="8de95-107">Jeśli parametr ReservationOrderId jest ustawiony, Pobierz określone ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="8de95-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="8de95-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8de95-108">EXAMPLES</span></span>

### <span data-ttu-id="8de95-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8de95-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="8de95-110">Lista wszystkich `ReservationOrder` użytkowników, do których użytkownik ma dostęp w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="8de95-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="8de95-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8de95-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="8de95-112">Zapoznaj `ReservationOrder` się z określoną ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8de95-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="8de95-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8de95-113">PARAMETERS</span></span>

### <span data-ttu-id="8de95-114">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8de95-114">-ReservationOrderId</span></span>
<span data-ttu-id="8de95-115">Identyfikator konkretnego ReservationOrder, który użytkownik chce zobaczyć</span><span class="sxs-lookup"><span data-stu-id="8de95-115">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="8de95-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de95-116">CommonParameters</span></span>
<span data-ttu-id="8de95-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de95-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de95-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de95-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de95-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8de95-119">INPUTS</span></span>

### <span data-ttu-id="8de95-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8de95-120">None</span></span>

## <span data-ttu-id="8de95-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8de95-121">OUTPUTS</span></span>

### <span data-ttu-id="8de95-122">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="8de95-122">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="8de95-123">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="8de95-123">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="8de95-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8de95-124">NOTES</span></span>

## <span data-ttu-id="8de95-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8de95-125">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 12e76c3412f54ba840528f9ff1a40acd388cd109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541539"
---
# <span data-ttu-id="f72ca-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f72ca-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="f72ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f72ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f72ca-103">Pobierz `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f72ca-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f72ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f72ca-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f72ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f72ca-105">DESCRIPTION</span></span>
<span data-ttu-id="f72ca-106">Lista wszystkich `ReservationOrder` osób, do których użytkownik ma dostęp w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="f72ca-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="f72ca-107">Jeśli parametr ReservationOrderId jest ustawiony, Pobierz określone ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="f72ca-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="f72ca-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f72ca-108">EXAMPLES</span></span>

### <span data-ttu-id="f72ca-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f72ca-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="f72ca-110">Lista wszystkich `ReservationOrder` użytkowników, do których użytkownik ma dostęp w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="f72ca-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="f72ca-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f72ca-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="f72ca-112">Zapoznaj `ReservationOrder` się z określoną ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f72ca-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="f72ca-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f72ca-113">PARAMETERS</span></span>

### <span data-ttu-id="f72ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72ca-114">-DefaultProfile</span></span>
<span data-ttu-id="f72ca-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f72ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f72ca-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f72ca-116">-ReservationOrderId</span></span>
<span data-ttu-id="f72ca-117">Identyfikator konkretnego ReservationOrder, który użytkownik chce zobaczyć</span><span class="sxs-lookup"><span data-stu-id="f72ca-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="f72ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72ca-118">CommonParameters</span></span>
<span data-ttu-id="f72ca-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72ca-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72ca-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72ca-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f72ca-121">INPUTS</span></span>

### <span data-ttu-id="f72ca-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f72ca-122">None</span></span>

## <span data-ttu-id="f72ca-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f72ca-123">OUTPUTS</span></span>

### <span data-ttu-id="f72ca-124">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="f72ca-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="f72ca-125">Microsoft. Azure. Commands. rezerwacje. modele. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f72ca-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="f72ca-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f72ca-126">NOTES</span></span>

## <span data-ttu-id="f72ca-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f72ca-127">RELATED LINKS</span></span>

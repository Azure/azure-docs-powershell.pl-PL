---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544159"
---
# <span data-ttu-id="ff8ba-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="ff8ba-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="ff8ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ff8ba-103">Pobieranie wykazu dostępnych rezerwacji</span><span class="sxs-lookup"><span data-stu-id="ff8ba-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff8ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff8ba-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff8ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ff8ba-105">DESCRIPTION</span></span>
<span data-ttu-id="ff8ba-106">Pobierz regiony i jednostki SKU, które są dostępne do zarezerwowanych zakupów wystąpienia dla określonej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff8ba-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="ff8ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff8ba-107">EXAMPLES</span></span>

### <span data-ttu-id="ff8ba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ff8ba-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="ff8ba-109">Pobieranie wykazu dla subskrypcji domyślnej</span><span class="sxs-lookup"><span data-stu-id="ff8ba-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="ff8ba-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ff8ba-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="ff8ba-111">Pobieranie wykazu dla określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ff8ba-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="ff8ba-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff8ba-112">PARAMETERS</span></span>

### <span data-ttu-id="ff8ba-113">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ff8ba-113">-SubscriptionId</span></span>
<span data-ttu-id="ff8ba-114">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ff8ba-114">Id of the subscription</span></span>

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

### <span data-ttu-id="ff8ba-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff8ba-115">CommonParameters</span></span>
<span data-ttu-id="ff8ba-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff8ba-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff8ba-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff8ba-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff8ba-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff8ba-118">INPUTS</span></span>

### <span data-ttu-id="ff8ba-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ff8ba-119">None</span></span>

## <span data-ttu-id="ff8ba-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff8ba-120">OUTPUTS</span></span>

### <span data-ttu-id="ff8ba-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. rezerwacje. modele. PSCatalog, Microsoft. Azure. Commands. rezerwacje, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ff8ba-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ff8ba-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff8ba-122">NOTES</span></span>

## <span data-ttu-id="ff8ba-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff8ba-123">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 155310764ea540d9062df8ae8f37171bc6f73066
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541540"
---
# <span data-ttu-id="510ac-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="510ac-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="510ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="510ac-102">SYNOPSIS</span></span>
<span data-ttu-id="510ac-103">Pobieranie wykazu dostępnych rezerwacji</span><span class="sxs-lookup"><span data-stu-id="510ac-103">Get the catalog of available reservations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="510ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="510ac-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="510ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="510ac-105">DESCRIPTION</span></span>
<span data-ttu-id="510ac-106">Pobierz regiony i jednostki SKU, które są dostępne do zarezerwowanych zakupów wystąpienia dla określonej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="510ac-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="510ac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="510ac-107">EXAMPLES</span></span>

### <span data-ttu-id="510ac-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="510ac-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="510ac-109">Pobieranie wykazu VirtualMachines na zachód dla subskrypcji domyślnej</span><span class="sxs-lookup"><span data-stu-id="510ac-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="510ac-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="510ac-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="510ac-111">Pobieranie wykazu SuseLinux dla określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="510ac-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="510ac-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="510ac-112">PARAMETERS</span></span>

### <span data-ttu-id="510ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510ac-113">-DefaultProfile</span></span>
<span data-ttu-id="510ac-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="510ac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="510ac-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="510ac-115">-Location</span></span>
<span data-ttu-id="510ac-116">Określa lokalizację zasobów zarezerwowanych w wykazie.</span><span class="sxs-lookup"><span data-stu-id="510ac-116">Specifies the location of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510ac-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="510ac-117">-ReservedResourceType</span></span>
<span data-ttu-id="510ac-118">Określa typ zasobów zarezerwowanych w wykazie.</span><span class="sxs-lookup"><span data-stu-id="510ac-118">Specifies the type of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510ac-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="510ac-119">-SubscriptionId</span></span>
<span data-ttu-id="510ac-120">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="510ac-120">Id of the subscription</span></span>

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

### <span data-ttu-id="510ac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510ac-121">CommonParameters</span></span>
<span data-ttu-id="510ac-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="510ac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510ac-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="510ac-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510ac-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="510ac-124">INPUTS</span></span>

### <span data-ttu-id="510ac-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="510ac-125">None</span></span>

## <span data-ttu-id="510ac-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="510ac-126">OUTPUTS</span></span>

### <span data-ttu-id="510ac-127">Microsoft. Azure. Commands. rezerwacje. modele. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="510ac-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="510ac-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="510ac-128">NOTES</span></span>

## <span data-ttu-id="510ac-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="510ac-129">RELATED LINKS</span></span>
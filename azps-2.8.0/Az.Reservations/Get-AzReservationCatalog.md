---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 2b470a9837fafbb20d2e83f6fa9e7b4308b12d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871919"
---
# <span data-ttu-id="6eddf-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="6eddf-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="6eddf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6eddf-102">SYNOPSIS</span></span>
<span data-ttu-id="6eddf-103">Pobieranie wykazu dostępnych rezerwacji</span><span class="sxs-lookup"><span data-stu-id="6eddf-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="6eddf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6eddf-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eddf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6eddf-105">DESCRIPTION</span></span>
<span data-ttu-id="6eddf-106">Pobierz regiony i jednostki SKU, które są dostępne do zarezerwowanych zakupów wystąpienia dla określonej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6eddf-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="6eddf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6eddf-107">EXAMPLES</span></span>

### <span data-ttu-id="6eddf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6eddf-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="6eddf-109">Pobieranie wykazu VirtualMachines na zachód dla subskrypcji domyślnej</span><span class="sxs-lookup"><span data-stu-id="6eddf-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="6eddf-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6eddf-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="6eddf-111">Pobieranie wykazu SuseLinux dla określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6eddf-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="6eddf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6eddf-112">PARAMETERS</span></span>

### <span data-ttu-id="6eddf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eddf-113">-DefaultProfile</span></span>
<span data-ttu-id="6eddf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6eddf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eddf-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6eddf-115">-Location</span></span>
<span data-ttu-id="6eddf-116">Określa lokalizację zasobów zarezerwowanych w wykazie.</span><span class="sxs-lookup"><span data-stu-id="6eddf-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="6eddf-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="6eddf-117">-ReservedResourceType</span></span>
<span data-ttu-id="6eddf-118">Określa typ zasobów zarezerwowanych w wykazie.</span><span class="sxs-lookup"><span data-stu-id="6eddf-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="6eddf-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6eddf-119">-SubscriptionId</span></span>
<span data-ttu-id="6eddf-120">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6eddf-120">Id of the subscription</span></span>

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

### <span data-ttu-id="6eddf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eddf-121">CommonParameters</span></span>
<span data-ttu-id="6eddf-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eddf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eddf-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eddf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eddf-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6eddf-124">INPUTS</span></span>

### <span data-ttu-id="6eddf-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6eddf-125">None</span></span>

## <span data-ttu-id="6eddf-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6eddf-126">OUTPUTS</span></span>

### <span data-ttu-id="6eddf-127">Microsoft. Azure. Commands. rezerwacje. modele. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="6eddf-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="6eddf-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6eddf-128">NOTES</span></span>

## <span data-ttu-id="6eddf-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6eddf-129">RELATED LINKS</span></span>

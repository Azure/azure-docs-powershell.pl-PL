---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240099"
---
# <span data-ttu-id="606c5-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="606c5-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="606c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="606c5-102">SYNOPSIS</span></span>
<span data-ttu-id="606c5-103">Pobierz katalog dostępnych rezerwacji</span><span class="sxs-lookup"><span data-stu-id="606c5-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="606c5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="606c5-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="606c5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="606c5-105">DESCRIPTION</span></span>
<span data-ttu-id="606c5-106">Pobierz regiony i jednostki SKU dostępne do zakupu w ramach zarezerwowanego wystąpienia dla określonej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="606c5-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="606c5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="606c5-107">EXAMPLES</span></span>

### <span data-ttu-id="606c5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="606c5-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="606c5-109">Pobierz katalog VirtualMachines w języku zachódus dla domyślnej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="606c5-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="606c5-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="606c5-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="606c5-111">Uzyskiwanie katalogu SuseLinux dla określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="606c5-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="606c5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="606c5-112">PARAMETERS</span></span>

### <span data-ttu-id="606c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606c5-113">-DefaultProfile</span></span>
<span data-ttu-id="606c5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="606c5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="606c5-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="606c5-115">-Location</span></span>
<span data-ttu-id="606c5-116">Określa lokalizację zastrzeżonych zasobów w wykazie.</span><span class="sxs-lookup"><span data-stu-id="606c5-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="606c5-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="606c5-117">-ReservedResourceType</span></span>
<span data-ttu-id="606c5-118">Określa typ zasobów zastrzeżonych w wykazie.</span><span class="sxs-lookup"><span data-stu-id="606c5-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="606c5-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="606c5-119">-SubscriptionId</span></span>
<span data-ttu-id="606c5-120">Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="606c5-120">Id of the subscription</span></span>

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

### <span data-ttu-id="606c5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606c5-121">CommonParameters</span></span>
<span data-ttu-id="606c5-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="606c5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606c5-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="606c5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606c5-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="606c5-124">INPUTS</span></span>

### <span data-ttu-id="606c5-125">Brak</span><span class="sxs-lookup"><span data-stu-id="606c5-125">None</span></span>

## <span data-ttu-id="606c5-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="606c5-126">OUTPUTS</span></span>

### <span data-ttu-id="606c5-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="606c5-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="606c5-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="606c5-128">NOTES</span></span>

## <span data-ttu-id="606c5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="606c5-129">RELATED LINKS</span></span>

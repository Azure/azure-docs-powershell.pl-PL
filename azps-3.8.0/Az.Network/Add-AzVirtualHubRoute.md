---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051507"
---
# <span data-ttu-id="aceef-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="aceef-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="aceef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aceef-102">SYNOPSIS</span></span>
<span data-ttu-id="aceef-103">Tworzy obiekt VirtualHubRoute, który może zostać przekazany jako parametr do polecenia Add-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="aceef-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="aceef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aceef-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aceef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aceef-105">DESCRIPTION</span></span>
<span data-ttu-id="aceef-106">Tworzy obiekt VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="aceef-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="aceef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aceef-107">EXAMPLES</span></span>

### <span data-ttu-id="aceef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aceef-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="aceef-109">Powyższe polecenie utworzy obiekt VirtualHubRoute, który może zostać dodany do zasobu VirtualHubRouteTable i ustawiony na VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="aceef-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="aceef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aceef-110">PARAMETERS</span></span>

### <span data-ttu-id="aceef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aceef-111">-DefaultProfile</span></span>
<span data-ttu-id="aceef-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aceef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceef-113">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="aceef-113">-Destination</span></span>
<span data-ttu-id="aceef-114">Lista miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="aceef-114">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceef-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="aceef-115">-DestinationType</span></span>
<span data-ttu-id="aceef-116">Typ lokalizacji docelowych.</span><span class="sxs-lookup"><span data-stu-id="aceef-116">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceef-117">-Następny skok</span><span class="sxs-lookup"><span data-stu-id="aceef-117">-NextHop</span></span>
<span data-ttu-id="aceef-118">Lista następnych przeskoków.</span><span class="sxs-lookup"><span data-stu-id="aceef-118">List of Next hops.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceef-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="aceef-119">-NextHopType</span></span>
<span data-ttu-id="aceef-120">Typ następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="aceef-120">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aceef-121">CommonParameters</span></span>
<span data-ttu-id="aceef-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aceef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aceef-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aceef-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aceef-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aceef-124">INPUTS</span></span>

### <span data-ttu-id="aceef-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aceef-125">None</span></span>

## <span data-ttu-id="aceef-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aceef-126">OUTPUTS</span></span>

### <span data-ttu-id="aceef-127">Microsoft. Azure. Commands. Network. models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="aceef-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="aceef-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aceef-128">NOTES</span></span>

## <span data-ttu-id="aceef-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aceef-129">RELATED LINKS</span></span>

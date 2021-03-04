---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: d90d25776f895bee47549dfb08a4588f0e446883
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979754"
---
# <span data-ttu-id="ff5fc-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ff5fc-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="ff5fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5fc-103">Tworzy obiekt VirtualHubRoute, który może być przekazywany jako parametr do Add-AzVirtualHubRouteTable użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="ff5fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff5fc-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff5fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff5fc-105">DESCRIPTION</span></span>
<span data-ttu-id="ff5fc-106">Tworzy obiekt VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="ff5fc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff5fc-107">EXAMPLES</span></span>

### <span data-ttu-id="ff5fc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ff5fc-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="ff5fc-109">Powyższe polecenie utworzy obiekt VirtualHubRoute, który można następnie dodać do zasobu VirtualHubRouteTable i ustawić jako wirtualną.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="ff5fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff5fc-110">PARAMETERS</span></span>

### <span data-ttu-id="ff5fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5fc-111">-DefaultProfile</span></span>
<span data-ttu-id="ff5fc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff5fc-113">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="ff5fc-113">-Destination</span></span>
<span data-ttu-id="ff5fc-114">Lista miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-114">List of Destinations.</span></span>

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

### <span data-ttu-id="ff5fc-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="ff5fc-115">-DestinationType</span></span>
<span data-ttu-id="ff5fc-116">Typ miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="ff5fc-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="ff5fc-117">-NextHop</span></span>
<span data-ttu-id="ff5fc-118">Lista następnych przeskoków.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-118">List of Next hops.</span></span>

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

### <span data-ttu-id="ff5fc-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="ff5fc-119">-NextHopType</span></span>
<span data-ttu-id="ff5fc-120">Typ następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="ff5fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5fc-121">CommonParameters</span></span>
<span data-ttu-id="ff5fc-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff5fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5fc-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff5fc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5fc-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff5fc-124">INPUTS</span></span>

### <span data-ttu-id="ff5fc-125">Brak</span><span class="sxs-lookup"><span data-stu-id="ff5fc-125">None</span></span>

## <span data-ttu-id="ff5fc-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff5fc-126">OUTPUTS</span></span>

### <span data-ttu-id="ff5fc-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ff5fc-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="ff5fc-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff5fc-128">NOTES</span></span>

## <span data-ttu-id="ff5fc-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff5fc-129">RELATED LINKS</span></span>

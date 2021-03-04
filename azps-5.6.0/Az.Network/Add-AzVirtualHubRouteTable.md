---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5cf2756297a932269f2aee87a248a1ba0eeed20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979745"
---
# <span data-ttu-id="30a9d-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30a9d-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="30a9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="30a9d-103">Tworzy zasób tabeli tras wirtualnego centrum, który jest podrzędnym zasobem aplikacji VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="30a9d-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="30a9d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30a9d-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30a9d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="30a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="30a9d-106">Zasób tabeli tras wirtualnego centrum zawiera listę tras oraz listę połączeń, do których można go dołączyć, i służy do rozsyłania ruchu w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="30a9d-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="30a9d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30a9d-107">EXAMPLES</span></span>

### <span data-ttu-id="30a9d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30a9d-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="30a9d-109">Powyższe polecenie utworzy zasób tabeli tras wirtualnego centrum z tras do niego przekazanych, a ten obiekt może być używany do routingu ruchu w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="30a9d-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="30a9d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30a9d-110">PARAMETERS</span></span>

### <span data-ttu-id="30a9d-111">— Połączenie</span><span class="sxs-lookup"><span data-stu-id="30a9d-111">-Connection</span></span>
<span data-ttu-id="30a9d-112">Lista połączeń, do których jest dołączona tabela trasy.</span><span class="sxs-lookup"><span data-stu-id="30a9d-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="30a9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a9d-113">-DefaultProfile</span></span>
<span data-ttu-id="30a9d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="30a9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a9d-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="30a9d-115">-Name</span></span>
<span data-ttu-id="30a9d-116">Nazwa tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="30a9d-116">Name of the route table.</span></span>

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

### <span data-ttu-id="30a9d-117">— Trasuj</span><span class="sxs-lookup"><span data-stu-id="30a9d-117">-Route</span></span>
<span data-ttu-id="30a9d-118">Lista tras centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="30a9d-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a9d-119">CommonParameters</span></span>
<span data-ttu-id="30a9d-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a9d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30a9d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a9d-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a9d-122">INPUTS</span></span>

### <span data-ttu-id="30a9d-123">Brak</span><span class="sxs-lookup"><span data-stu-id="30a9d-123">None</span></span>

## <span data-ttu-id="30a9d-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a9d-124">OUTPUTS</span></span>

### <span data-ttu-id="30a9d-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30a9d-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="30a9d-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30a9d-126">NOTES</span></span>

## <span data-ttu-id="30a9d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30a9d-127">RELATED LINKS</span></span>

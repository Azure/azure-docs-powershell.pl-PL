---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: 0d798c5eb70c8c472862e9af0f992d01827a750e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954074"
---
# <span data-ttu-id="823f1-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="823f1-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="823f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="823f1-102">SYNOPSIS</span></span>
<span data-ttu-id="823f1-103">Pobiera element równorzędny serwera trasy w usłudze Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="823f1-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="823f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="823f1-104">SYNTAX</span></span>

### <span data-ttu-id="823f1-105">RouteServerNPeerNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="823f1-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="823f1-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="823f1-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="823f1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="823f1-107">DESCRIPTION</span></span>
<span data-ttu-id="823f1-108">Polecenie **cmdlet Get-AzRouteServerPeer** pobiera element równorzędny w usłudze Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="823f1-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="823f1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="823f1-109">EXAMPLES</span></span>

### <span data-ttu-id="823f1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="823f1-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="823f1-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="823f1-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="823f1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="823f1-112">PARAMETERS</span></span>

### <span data-ttu-id="823f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="823f1-113">-DefaultProfile</span></span>
<span data-ttu-id="823f1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="823f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="823f1-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="823f1-115">-PeerName</span></span>
<span data-ttu-id="823f1-116">Nazwa elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="823f1-116">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="823f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="823f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="823f1-118">Nazwa grupy zasobów serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="823f1-118">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="823f1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="823f1-119">-ResourceId</span></span>
<span data-ttu-id="823f1-120">ResourceId elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="823f1-120">ResourceId of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="823f1-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="823f1-121">-RouteServerName</span></span>
<span data-ttu-id="823f1-122">Nazwa serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="823f1-122">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="823f1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="823f1-123">CommonParameters</span></span>
<span data-ttu-id="823f1-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="823f1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="823f1-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="823f1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="823f1-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="823f1-126">INPUTS</span></span>

### <span data-ttu-id="823f1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="823f1-127">System.String</span></span>

## <span data-ttu-id="823f1-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="823f1-128">OUTPUTS</span></span>

### <span data-ttu-id="823f1-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="823f1-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="823f1-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="823f1-130">NOTES</span></span>

## <span data-ttu-id="823f1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="823f1-131">RELATED LINKS</span></span>

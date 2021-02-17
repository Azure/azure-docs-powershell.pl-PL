---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: d36a919adfbf1a7a2e2b7a10313433e820cc478a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184667"
---
# <span data-ttu-id="bfd8e-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="bfd8e-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="bfd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd8e-103">Pobiera element równorzędny serwera trasy w usłudze Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="bfd8e-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="bfd8e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bfd8e-104">SYNTAX</span></span>

### <span data-ttu-id="bfd8e-105">RouteServerNPeerNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="bfd8e-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfd8e-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd8e-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfd8e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bfd8e-107">DESCRIPTION</span></span>
<span data-ttu-id="bfd8e-108">Polecenie **cmdlet Get-AzRouteServerPeer** pobiera element równorzędny w usłudze Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="bfd8e-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="bfd8e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bfd8e-109">EXAMPLES</span></span>

### <span data-ttu-id="bfd8e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bfd8e-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="bfd8e-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bfd8e-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="bfd8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfd8e-112">PARAMETERS</span></span>

### <span data-ttu-id="bfd8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd8e-113">-DefaultProfile</span></span>
<span data-ttu-id="bfd8e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfd8e-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="bfd8e-115">-PeerName</span></span>
<span data-ttu-id="bfd8e-116">Nazwa elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-116">The name of the route server peer.</span></span>

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

### <span data-ttu-id="bfd8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="bfd8e-118">Nazwa grupy zasobów serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-118">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="bfd8e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfd8e-119">-ResourceId</span></span>
<span data-ttu-id="bfd8e-120">ResourceId elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-120">ResourceId of the route server peer.</span></span>

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

### <span data-ttu-id="bfd8e-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="bfd8e-121">-RouteServerName</span></span>
<span data-ttu-id="bfd8e-122">Nazwa serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-122">The name of the route server.</span></span>

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

### <span data-ttu-id="bfd8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd8e-123">CommonParameters</span></span>
<span data-ttu-id="bfd8e-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd8e-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfd8e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd8e-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfd8e-126">INPUTS</span></span>

### <span data-ttu-id="bfd8e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bfd8e-127">System.String</span></span>

## <span data-ttu-id="bfd8e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bfd8e-128">OUTPUTS</span></span>

### <span data-ttu-id="bfd8e-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="bfd8e-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="bfd8e-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bfd8e-130">NOTES</span></span>

## <span data-ttu-id="bfd8e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfd8e-131">RELATED LINKS</span></span>

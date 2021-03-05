---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: 52733af41b5f8d84811f1c1f184181a2d45053e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982314"
---
# <span data-ttu-id="138e1-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="138e1-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="138e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="138e1-102">SYNOPSIS</span></span>
<span data-ttu-id="138e1-103">Usuwa elementu równorzędnego z serwera usługi Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="138e1-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="138e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="138e1-104">SYNTAX</span></span>

### <span data-ttu-id="138e1-105">RouteServerNPeerNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="138e1-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="138e1-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="138e1-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="138e1-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="138e1-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="138e1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="138e1-108">DESCRIPTION</span></span>
<span data-ttu-id="138e1-109">Polecenie **cmdlet Remove-AzRouteServerPeer** usuwa element równorzędny serwera trasy z serwera azure routeserver</span><span class="sxs-lookup"><span data-stu-id="138e1-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="138e1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="138e1-110">EXAMPLES</span></span>

### <span data-ttu-id="138e1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="138e1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="138e1-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="138e1-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="138e1-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="138e1-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="138e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="138e1-114">PARAMETERS</span></span>

### <span data-ttu-id="138e1-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="138e1-115">-AsJob</span></span>
<span data-ttu-id="138e1-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="138e1-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="138e1-117">-DefaultProfile</span></span>
<span data-ttu-id="138e1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="138e1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="138e1-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="138e1-119">-Force</span></span>
<span data-ttu-id="138e1-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="138e1-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138e1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="138e1-121">-InputObject</span></span>
<span data-ttu-id="138e1-122">Obiekt wejściowy równorzędny serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="138e1-122">The route server peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer
Parameter Sets: RouteServerNPeerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="138e1-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="138e1-123">-PeerName</span></span>
<span data-ttu-id="138e1-124">Nazwa elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="138e1-124">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="138e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="138e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="138e1-126">Nazwa grupy zasobów serwera/elementu równorzędnego trasy.</span><span class="sxs-lookup"><span data-stu-id="138e1-126">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="138e1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="138e1-127">-ResourceId</span></span>
<span data-ttu-id="138e1-128">Identyfikator zasobu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="138e1-128">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="138e1-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="138e1-129">-RouteServerName</span></span>
<span data-ttu-id="138e1-130">Serwer trasy, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="138e1-130">The route server where peer exists.</span></span>

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

### <span data-ttu-id="138e1-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="138e1-131">-Confirm</span></span>
<span data-ttu-id="138e1-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="138e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="138e1-133">-WhatIf</span></span>
<span data-ttu-id="138e1-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="138e1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="138e1-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="138e1-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="138e1-136">CommonParameters</span></span>
<span data-ttu-id="138e1-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="138e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="138e1-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="138e1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="138e1-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="138e1-139">INPUTS</span></span>

### <span data-ttu-id="138e1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="138e1-140">System.String</span></span>

### <span data-ttu-id="138e1-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="138e1-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="138e1-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="138e1-142">OUTPUTS</span></span>

### <span data-ttu-id="138e1-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="138e1-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="138e1-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="138e1-144">NOTES</span></span>

## <span data-ttu-id="138e1-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="138e1-145">RELATED LINKS</span></span>

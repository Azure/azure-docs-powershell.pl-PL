---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: d177c0dfa5ff59fde0adfe8ac4e3598ae70127f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202535"
---
# <span data-ttu-id="a6243-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="a6243-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="a6243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6243-102">SYNOPSIS</span></span>
<span data-ttu-id="a6243-103">Usuwa elementu równorzędnego z serwera usługi Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="a6243-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="a6243-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6243-104">SYNTAX</span></span>

### <span data-ttu-id="a6243-105">RouteServerNPeerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a6243-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6243-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6243-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6243-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6243-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6243-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6243-108">DESCRIPTION</span></span>
<span data-ttu-id="a6243-109">Polecenie **cmdlet Remove-AzRouteServerPeer** usuwa element równorzędny serwera trasy z serwera azure routeserver</span><span class="sxs-lookup"><span data-stu-id="a6243-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="a6243-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6243-110">EXAMPLES</span></span>

### <span data-ttu-id="a6243-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6243-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="a6243-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a6243-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="a6243-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a6243-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="a6243-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6243-114">PARAMETERS</span></span>

### <span data-ttu-id="a6243-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a6243-115">-AsJob</span></span>
<span data-ttu-id="a6243-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a6243-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6243-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6243-117">-DefaultProfile</span></span>
<span data-ttu-id="a6243-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6243-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6243-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a6243-119">-Force</span></span>
<span data-ttu-id="a6243-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="a6243-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a6243-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6243-121">-InputObject</span></span>
<span data-ttu-id="a6243-122">Obiekt wejściowy równorzędny serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="a6243-122">The route server peer input object.</span></span>

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

### <span data-ttu-id="a6243-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="a6243-123">-PeerName</span></span>
<span data-ttu-id="a6243-124">Nazwa elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="a6243-124">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="a6243-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6243-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6243-126">Nazwa grupy zasobów serwera/elementu równorzędnego trasy.</span><span class="sxs-lookup"><span data-stu-id="a6243-126">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="a6243-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6243-127">-ResourceId</span></span>
<span data-ttu-id="a6243-128">Identyfikator zasobu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="a6243-128">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="a6243-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="a6243-129">-RouteServerName</span></span>
<span data-ttu-id="a6243-130">Serwer trasy, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="a6243-130">The route server where peer exists.</span></span>

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

### <span data-ttu-id="a6243-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6243-131">-Confirm</span></span>
<span data-ttu-id="a6243-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6243-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6243-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6243-133">-WhatIf</span></span>
<span data-ttu-id="a6243-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6243-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6243-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a6243-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6243-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6243-136">CommonParameters</span></span>
<span data-ttu-id="a6243-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6243-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6243-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6243-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6243-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6243-139">INPUTS</span></span>

### <span data-ttu-id="a6243-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a6243-140">System.String</span></span>

### <span data-ttu-id="a6243-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="a6243-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="a6243-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6243-142">OUTPUTS</span></span>

### <span data-ttu-id="a6243-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="a6243-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="a6243-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6243-144">NOTES</span></span>

## <span data-ttu-id="a6243-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6243-145">RELATED LINKS</span></span>

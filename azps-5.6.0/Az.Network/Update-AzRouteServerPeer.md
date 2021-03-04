---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 3c0be49a09758648bcd2301f2643577ea8dcd951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951610"
---
# <span data-ttu-id="3074f-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="3074f-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="3074f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3074f-102">SYNOPSIS</span></span>
<span data-ttu-id="3074f-103">Aktualizowanie elementu równorzędnego w usłudze Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="3074f-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="3074f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3074f-104">SYNTAX</span></span>

### <span data-ttu-id="3074f-105">RouteServerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3074f-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3074f-106">RouteServerNPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3074f-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3074f-107">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3074f-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3074f-108">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3074f-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3074f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="3074f-109">DESCRIPTION</span></span>
<span data-ttu-id="3074f-110">Polecenie **cmdlet Update-AzRouteServerPeer** aktualizuje element równorzędny serwera trasy na serwerze azure routeserver</span><span class="sxs-lookup"><span data-stu-id="3074f-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="3074f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3074f-111">EXAMPLES</span></span>

### <span data-ttu-id="3074f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3074f-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="3074f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3074f-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="3074f-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3074f-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="3074f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3074f-115">PARAMETERS</span></span>

### <span data-ttu-id="3074f-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3074f-116">-AsJob</span></span>
<span data-ttu-id="3074f-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3074f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3074f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3074f-118">-DefaultProfile</span></span>
<span data-ttu-id="3074f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3074f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3074f-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3074f-120">-Force</span></span>
<span data-ttu-id="3074f-121">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="3074f-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3074f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3074f-122">-InputObject</span></span>
<span data-ttu-id="3074f-123">Obiekt wejściowy równorzędny serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="3074f-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="3074f-124">- PeerAsn</span><span class="sxs-lookup"><span data-stu-id="3074f-124">-PeerAsn</span></span>
<span data-ttu-id="3074f-125">ASN elementu równorzędnego serwera trasy zdalnej.</span><span class="sxs-lookup"><span data-stu-id="3074f-125">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3074f-126">— Komunikacja równorzędna</span><span class="sxs-lookup"><span data-stu-id="3074f-126">-PeerIp</span></span>
<span data-ttu-id="3074f-127">Ip elementu równorzędnego serwera trasy zdalnej.</span><span class="sxs-lookup"><span data-stu-id="3074f-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="3074f-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="3074f-128">-PeerName</span></span>
<span data-ttu-id="3074f-129">Nazwa elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="3074f-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="3074f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3074f-130">-ResourceGroupName</span></span>
<span data-ttu-id="3074f-131">Nazwa grupy zasobów serwera/elementu równorzędnego trasy.</span><span class="sxs-lookup"><span data-stu-id="3074f-131">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3074f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3074f-132">-ResourceId</span></span>
<span data-ttu-id="3074f-133">Identyfikator zasobu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="3074f-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="3074f-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="3074f-134">-RouteServerName</span></span>
<span data-ttu-id="3074f-135">Serwer trasy, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="3074f-135">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3074f-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3074f-136">-Confirm</span></span>
<span data-ttu-id="3074f-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3074f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3074f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3074f-138">-WhatIf</span></span>
<span data-ttu-id="3074f-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3074f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3074f-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3074f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3074f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3074f-141">CommonParameters</span></span>
<span data-ttu-id="3074f-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3074f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3074f-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3074f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3074f-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3074f-144">INPUTS</span></span>

### <span data-ttu-id="3074f-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3074f-145">System.String</span></span>

### <span data-ttu-id="3074f-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="3074f-146">System.UInt32</span></span>

### <span data-ttu-id="3074f-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="3074f-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="3074f-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3074f-148">OUTPUTS</span></span>

### <span data-ttu-id="3074f-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="3074f-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="3074f-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3074f-150">NOTES</span></span>

## <span data-ttu-id="3074f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3074f-151">RELATED LINKS</span></span>

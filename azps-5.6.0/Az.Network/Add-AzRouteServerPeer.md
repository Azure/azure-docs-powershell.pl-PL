---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 430292ba3a387a0b2a0285b26c147c375f114398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979777"
---
# <span data-ttu-id="e2ad0-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="e2ad0-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="e2ad0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ad0-103">Dodawanie elementu równorzędnego do serwera usługi Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="e2ad0-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="e2ad0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e2ad0-104">SYNTAX</span></span>

### <span data-ttu-id="e2ad0-105">RouteServerNPeerNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="e2ad0-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2ad0-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2ad0-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2ad0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e2ad0-107">DESCRIPTION</span></span>
<span data-ttu-id="e2ad0-108">Polecenie **cmdlet Add-AzRouteServerPeer** dodaje element równorzędny serwera trasy do serwera trasy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e2ad0-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="e2ad0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e2ad0-109">EXAMPLES</span></span>

### <span data-ttu-id="e2ad0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2ad0-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="e2ad0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2ad0-111">PARAMETERS</span></span>

### <span data-ttu-id="e2ad0-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e2ad0-112">-AsJob</span></span>
<span data-ttu-id="e2ad0-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e2ad0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2ad0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ad0-114">-DefaultProfile</span></span>
<span data-ttu-id="e2ad0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ad0-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e2ad0-116">-Force</span></span>
<span data-ttu-id="e2ad0-117">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="e2ad0-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e2ad0-118">- PeerAsn</span><span class="sxs-lookup"><span data-stu-id="e2ad0-118">-PeerAsn</span></span>
<span data-ttu-id="e2ad0-119">ASN elementu równorzędnego serwera trasy zdalnej.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-119">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ad0-120">— Komunikacja równorzędna</span><span class="sxs-lookup"><span data-stu-id="e2ad0-120">-PeerIp</span></span>
<span data-ttu-id="e2ad0-121">Ip elementu równorzędnego serwera trasy zdalnej.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="e2ad0-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="e2ad0-122">-PeerName</span></span>
<span data-ttu-id="e2ad0-123">Nazwa elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-123">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ad0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ad0-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2ad0-125">Nazwa grupy zasobów serwera/elementu równorzędnego trasy.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="e2ad0-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="e2ad0-126">-RouteServerName</span></span>
<span data-ttu-id="e2ad0-127">Serwer trasy, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-127">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ad0-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2ad0-128">-Confirm</span></span>
<span data-ttu-id="e2ad0-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ad0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ad0-130">-WhatIf</span></span>
<span data-ttu-id="e2ad0-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ad0-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ad0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ad0-133">CommonParameters</span></span>
<span data-ttu-id="e2ad0-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ad0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ad0-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2ad0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ad0-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2ad0-136">INPUTS</span></span>

### <span data-ttu-id="e2ad0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e2ad0-137">System.String</span></span>

### <span data-ttu-id="e2ad0-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="e2ad0-138">System.UInt32</span></span>

## <span data-ttu-id="e2ad0-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2ad0-139">OUTPUTS</span></span>

### <span data-ttu-id="e2ad0-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="e2ad0-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="e2ad0-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e2ad0-141">NOTES</span></span>

## <span data-ttu-id="e2ad0-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2ad0-142">RELATED LINKS</span></span>

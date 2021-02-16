---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 70f7573a604ea15c33f1949883503fed2a356e00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192018"
---
# <span data-ttu-id="10841-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="10841-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="10841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10841-102">SYNOPSIS</span></span>
<span data-ttu-id="10841-103">Dodawanie elementu równorzędnego do serwera usługi Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="10841-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="10841-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10841-104">SYNTAX</span></span>

### <span data-ttu-id="10841-105">RouteServerNPeerNameParameterSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="10841-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10841-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10841-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10841-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="10841-107">DESCRIPTION</span></span>
<span data-ttu-id="10841-108">Polecenie **cmdlet Add-AzRouteServerPeer** dodaje element równorzędny serwera trasy do serwera trasy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="10841-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="10841-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10841-109">EXAMPLES</span></span>

### <span data-ttu-id="10841-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10841-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="10841-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10841-111">PARAMETERS</span></span>

### <span data-ttu-id="10841-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="10841-112">-AsJob</span></span>
<span data-ttu-id="10841-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="10841-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10841-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10841-114">-DefaultProfile</span></span>
<span data-ttu-id="10841-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10841-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10841-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="10841-116">-Force</span></span>
<span data-ttu-id="10841-117">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="10841-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="10841-118">- PeerAsn</span><span class="sxs-lookup"><span data-stu-id="10841-118">-PeerAsn</span></span>
<span data-ttu-id="10841-119">ASN elementu równorzędnego serwera trasy zdalnej.</span><span class="sxs-lookup"><span data-stu-id="10841-119">ASN of remote route server peer.</span></span>

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

### <span data-ttu-id="10841-120">— Komunikacja równorzędna</span><span class="sxs-lookup"><span data-stu-id="10841-120">-PeerIp</span></span>
<span data-ttu-id="10841-121">Ip elementu równorzędnego serwera trasy zdalnej.</span><span class="sxs-lookup"><span data-stu-id="10841-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="10841-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="10841-122">-PeerName</span></span>
<span data-ttu-id="10841-123">Nazwa elementu równorzędnego serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="10841-123">The name of the route server peer.</span></span>

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

### <span data-ttu-id="10841-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10841-124">-ResourceGroupName</span></span>
<span data-ttu-id="10841-125">Nazwa grupy zasobów serwera/elementu równorzędnego trasy.</span><span class="sxs-lookup"><span data-stu-id="10841-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="10841-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="10841-126">-RouteServerName</span></span>
<span data-ttu-id="10841-127">Serwer trasy, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="10841-127">The route server where peer exists.</span></span>

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

### <span data-ttu-id="10841-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10841-128">-Confirm</span></span>
<span data-ttu-id="10841-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10841-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10841-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10841-130">-WhatIf</span></span>
<span data-ttu-id="10841-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10841-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10841-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10841-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10841-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10841-133">CommonParameters</span></span>
<span data-ttu-id="10841-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10841-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10841-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10841-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10841-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10841-136">INPUTS</span></span>

### <span data-ttu-id="10841-137">System.String</span><span class="sxs-lookup"><span data-stu-id="10841-137">System.String</span></span>

### <span data-ttu-id="10841-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="10841-138">System.UInt32</span></span>

## <span data-ttu-id="10841-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10841-139">OUTPUTS</span></span>

### <span data-ttu-id="10841-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="10841-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="10841-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10841-141">NOTES</span></span>

## <span data-ttu-id="10841-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10841-142">RELATED LINKS</span></span>

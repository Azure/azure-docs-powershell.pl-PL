---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: aae01212b44eebf03207f2b0bfed788992acbc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015073"
---
# <span data-ttu-id="c037e-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="c037e-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="c037e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c037e-102">SYNOPSIS</span></span>
<span data-ttu-id="c037e-103">Lista tras ogłaszanych przez określonego wirtualnego routera równorzędnego</span><span class="sxs-lookup"><span data-stu-id="c037e-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="c037e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c037e-104">SYNTAX</span></span>

### <span data-ttu-id="c037e-105">VirtualRouterPeerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c037e-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c037e-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c037e-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c037e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c037e-107">DESCRIPTION</span></span>
<span data-ttu-id="c037e-108">Jeśli dany router wirtualny jest równorzędny według nazwy lub obiektu, wylicza trasy ogłaszane do tej równorzędnej przez konkretny router wirtualny.</span><span class="sxs-lookup"><span data-stu-id="c037e-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="c037e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c037e-109">EXAMPLES</span></span>

### <span data-ttu-id="c037e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c037e-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="c037e-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c037e-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="c037e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c037e-112">PARAMETERS</span></span>

### <span data-ttu-id="c037e-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c037e-113">-AsJob</span></span>
<span data-ttu-id="c037e-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c037e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c037e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c037e-115">-DefaultProfile</span></span>
<span data-ttu-id="c037e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c037e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c037e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c037e-117">-InputObject</span></span>
<span data-ttu-id="c037e-118">Obiekt wejściowy równorzędny routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="c037e-118">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c037e-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c037e-119">-PeerName</span></span>
<span data-ttu-id="c037e-120">Nazwa równorzędnego routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="c037e-120">Virtual router peer name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c037e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c037e-121">-ResourceGroupName</span></span>
<span data-ttu-id="c037e-122">Nazwa grupy zasobów równorzędnych routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="c037e-122">Virtual router peer resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c037e-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="c037e-123">-VirtualRouterName</span></span>
<span data-ttu-id="c037e-124">Nazwa routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="c037e-124">Virtual router name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c037e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c037e-125">CommonParameters</span></span>
<span data-ttu-id="c037e-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c037e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c037e-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c037e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c037e-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c037e-128">INPUTS</span></span>

### <span data-ttu-id="c037e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c037e-129">System.String</span></span>

### <span data-ttu-id="c037e-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c037e-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="c037e-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c037e-131">OUTPUTS</span></span>

### <span data-ttu-id="c037e-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="c037e-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="c037e-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c037e-133">NOTES</span></span>

## <span data-ttu-id="c037e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c037e-134">RELATED LINKS</span></span>

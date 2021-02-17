---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184587"
---
# <span data-ttu-id="a98b6-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="a98b6-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="a98b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a98b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a98b6-103">Lista tras poznanych przez określonego wirtualnego routera równorzędnego</span><span class="sxs-lookup"><span data-stu-id="a98b6-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="a98b6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a98b6-104">SYNTAX</span></span>

### <span data-ttu-id="a98b6-105">VirtualRouterPeerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a98b6-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a98b6-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a98b6-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a98b6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a98b6-107">DESCRIPTION</span></span>
<span data-ttu-id="a98b6-108">Wyliczanie tras poznanych przez wirtualnego routera równorzędnego z innych źródeł.</span><span class="sxs-lookup"><span data-stu-id="a98b6-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="a98b6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a98b6-109">EXAMPLES</span></span>

### <span data-ttu-id="a98b6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a98b6-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="a98b6-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a98b6-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="a98b6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a98b6-112">PARAMETERS</span></span>

### <span data-ttu-id="a98b6-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a98b6-113">-AsJob</span></span>
<span data-ttu-id="a98b6-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a98b6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a98b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98b6-115">-DefaultProfile</span></span>
<span data-ttu-id="a98b6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a98b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a98b6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a98b6-117">-InputObject</span></span>
<span data-ttu-id="a98b6-118">Obiekt wejściowy równorzędny routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a98b6-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="a98b6-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="a98b6-119">-PeerName</span></span>
<span data-ttu-id="a98b6-120">Nazwa równorzędnego routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="a98b6-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="a98b6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a98b6-121">-ResourceGroupName</span></span>
<span data-ttu-id="a98b6-122">Nazwa grupy zasobów równorzędnych routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="a98b6-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="a98b6-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="a98b6-123">-VirtualRouterName</span></span>
<span data-ttu-id="a98b6-124">Nazwa routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="a98b6-124">Virtual router name</span></span>

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

### <span data-ttu-id="a98b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98b6-125">CommonParameters</span></span>
<span data-ttu-id="a98b6-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a98b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98b6-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a98b6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98b6-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a98b6-128">INPUTS</span></span>

### <span data-ttu-id="a98b6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a98b6-129">System.String</span></span>

### <span data-ttu-id="a98b6-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="a98b6-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="a98b6-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a98b6-131">OUTPUTS</span></span>

### <span data-ttu-id="a98b6-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="a98b6-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="a98b6-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a98b6-133">NOTES</span></span>

## <span data-ttu-id="a98b6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a98b6-134">RELATED LINKS</span></span>

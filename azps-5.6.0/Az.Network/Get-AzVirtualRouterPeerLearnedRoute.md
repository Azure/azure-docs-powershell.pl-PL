---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 99f76a12afdbc883d990fff5a05e06e2880aecf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985888"
---
# <span data-ttu-id="d09b1-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="d09b1-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="d09b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d09b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d09b1-103">Lista tras poznanych przez określonego współpracownika routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="d09b1-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="d09b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d09b1-104">SYNTAX</span></span>

### <span data-ttu-id="d09b1-105">VirtualRouterPeerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d09b1-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d09b1-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d09b1-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d09b1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d09b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d09b1-108">Wyliczanie tras poznanych przez wirtualnego routera równorzędnego z innych źródeł.</span><span class="sxs-lookup"><span data-stu-id="d09b1-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="d09b1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d09b1-109">EXAMPLES</span></span>

### <span data-ttu-id="d09b1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d09b1-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="d09b1-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d09b1-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="d09b1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d09b1-112">PARAMETERS</span></span>

### <span data-ttu-id="d09b1-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d09b1-113">-AsJob</span></span>
<span data-ttu-id="d09b1-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d09b1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d09b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d09b1-115">-DefaultProfile</span></span>
<span data-ttu-id="d09b1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d09b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d09b1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d09b1-117">-InputObject</span></span>
<span data-ttu-id="d09b1-118">Obiekt wejściowy równorzędny routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="d09b1-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="d09b1-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="d09b1-119">-PeerName</span></span>
<span data-ttu-id="d09b1-120">Nazwa równorzędnego routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="d09b1-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="d09b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d09b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="d09b1-122">Nazwa grupy zasobów równorzędnych routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="d09b1-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="d09b1-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="d09b1-123">-VirtualRouterName</span></span>
<span data-ttu-id="d09b1-124">Nazwa routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="d09b1-124">Virtual router name</span></span>

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

### <span data-ttu-id="d09b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d09b1-125">CommonParameters</span></span>
<span data-ttu-id="d09b1-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d09b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d09b1-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d09b1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d09b1-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d09b1-128">INPUTS</span></span>

### <span data-ttu-id="d09b1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d09b1-129">System.String</span></span>

### <span data-ttu-id="d09b1-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d09b1-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="d09b1-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d09b1-131">OUTPUTS</span></span>

### <span data-ttu-id="d09b1-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="d09b1-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="d09b1-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d09b1-133">NOTES</span></span>

## <span data-ttu-id="d09b1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d09b1-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225867"
---
# <span data-ttu-id="09038-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="09038-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="09038-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09038-102">SYNOPSIS</span></span>
<span data-ttu-id="09038-103">Wyświetlanie listy tras rozstawionych przez określony węzeł wirtualny routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="09038-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="09038-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09038-104">SYNTAX</span></span>

### <span data-ttu-id="09038-105">VirtualRouterPeerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="09038-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09038-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09038-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09038-107">Opis</span><span class="sxs-lookup"><span data-stu-id="09038-107">DESCRIPTION</span></span>
<span data-ttu-id="09038-108">Wyliczanie tras rozliczonych przez element równorzędny wirtualnego routera z innych źródeł.</span><span class="sxs-lookup"><span data-stu-id="09038-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="09038-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09038-109">EXAMPLES</span></span>

### <span data-ttu-id="09038-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09038-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="09038-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="09038-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="09038-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09038-112">PARAMETERS</span></span>

### <span data-ttu-id="09038-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09038-113">-AsJob</span></span>
<span data-ttu-id="09038-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="09038-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09038-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09038-115">-DefaultProfile</span></span>
<span data-ttu-id="09038-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09038-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09038-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09038-117">-InputObject</span></span>
<span data-ttu-id="09038-118">Obiekt wejściowy peer routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="09038-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="09038-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="09038-119">-PeerName</span></span>
<span data-ttu-id="09038-120">Nazwa węzła równorzędnego routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="09038-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="09038-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09038-121">-ResourceGroupName</span></span>
<span data-ttu-id="09038-122">Nazwa grupy zasobów równorzędnych routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="09038-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="09038-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="09038-123">-VirtualRouterName</span></span>
<span data-ttu-id="09038-124">Nazwa routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="09038-124">Virtual router name</span></span>

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

### <span data-ttu-id="09038-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09038-125">CommonParameters</span></span>
<span data-ttu-id="09038-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09038-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09038-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09038-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09038-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09038-128">INPUTS</span></span>

### <span data-ttu-id="09038-129">System. String</span><span class="sxs-lookup"><span data-stu-id="09038-129">System.String</span></span>

### <span data-ttu-id="09038-130">Microsoft. Azure. Commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="09038-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="09038-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09038-131">OUTPUTS</span></span>

### <span data-ttu-id="09038-132">Microsoft. Azure. Commands. Network. models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="09038-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="09038-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09038-133">NOTES</span></span>

## <span data-ttu-id="09038-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09038-134">RELATED LINKS</span></span>

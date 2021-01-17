---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352681"
---
# <span data-ttu-id="d57fb-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="d57fb-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="d57fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d57fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d57fb-103">Wyświetlanie listy tras rozstawionych przez określony węzeł wirtualny routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="d57fb-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="d57fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d57fb-104">SYNTAX</span></span>

### <span data-ttu-id="d57fb-105">VirtualRouterPeerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d57fb-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d57fb-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d57fb-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d57fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d57fb-107">DESCRIPTION</span></span>
<span data-ttu-id="d57fb-108">Wyliczanie tras rozliczonych przez element równorzędny wirtualnego routera z innych źródeł.</span><span class="sxs-lookup"><span data-stu-id="d57fb-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="d57fb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d57fb-109">EXAMPLES</span></span>

### <span data-ttu-id="d57fb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d57fb-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="d57fb-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d57fb-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="d57fb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d57fb-112">PARAMETERS</span></span>

### <span data-ttu-id="d57fb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d57fb-113">-AsJob</span></span>
<span data-ttu-id="d57fb-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d57fb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d57fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57fb-115">-DefaultProfile</span></span>
<span data-ttu-id="d57fb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d57fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d57fb-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d57fb-117">-InputObject</span></span>
<span data-ttu-id="d57fb-118">Obiekt wejściowy peer routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="d57fb-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="d57fb-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="d57fb-119">-PeerName</span></span>
<span data-ttu-id="d57fb-120">Nazwa węzła równorzędnego routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="d57fb-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="d57fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="d57fb-122">Nazwa grupy zasobów równorzędnych routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="d57fb-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="d57fb-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="d57fb-123">-VirtualRouterName</span></span>
<span data-ttu-id="d57fb-124">Nazwa routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="d57fb-124">Virtual router name</span></span>

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

### <span data-ttu-id="d57fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57fb-125">CommonParameters</span></span>
<span data-ttu-id="d57fb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d57fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57fb-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d57fb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57fb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d57fb-128">INPUTS</span></span>

### <span data-ttu-id="d57fb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d57fb-129">System.String</span></span>

### <span data-ttu-id="d57fb-130">Microsoft. Azure. Commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d57fb-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="d57fb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d57fb-131">OUTPUTS</span></span>

### <span data-ttu-id="d57fb-132">Microsoft. Azure. Commands. Network. models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="d57fb-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="d57fb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d57fb-133">NOTES</span></span>

## <span data-ttu-id="d57fb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d57fb-134">RELATED LINKS</span></span>

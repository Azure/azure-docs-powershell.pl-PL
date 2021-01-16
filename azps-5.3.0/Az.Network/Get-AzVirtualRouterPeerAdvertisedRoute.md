---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379785"
---
# <span data-ttu-id="a05b5-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="a05b5-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="a05b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a05b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a05b5-103">Lista tras anonsowanych przez określony element równorzędny wirtualnego routera</span><span class="sxs-lookup"><span data-stu-id="a05b5-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="a05b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a05b5-104">SYNTAX</span></span>

### <span data-ttu-id="a05b5-105">VirtualRouterPeerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a05b5-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a05b5-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a05b5-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a05b5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a05b5-107">DESCRIPTION</span></span>
<span data-ttu-id="a05b5-108">W przypadku elementu równorzędnego routera wirtualnego należy wyliczyć trasy anonsowane na tym elemencie równorzędnym przez określony router wirtualny.</span><span class="sxs-lookup"><span data-stu-id="a05b5-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="a05b5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a05b5-109">EXAMPLES</span></span>

### <span data-ttu-id="a05b5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a05b5-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="a05b5-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a05b5-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="a05b5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a05b5-112">PARAMETERS</span></span>

### <span data-ttu-id="a05b5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a05b5-113">-AsJob</span></span>
<span data-ttu-id="a05b5-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a05b5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a05b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05b5-115">-DefaultProfile</span></span>
<span data-ttu-id="a05b5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a05b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05b5-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a05b5-117">-InputObject</span></span>
<span data-ttu-id="a05b5-118">Obiekt wejściowy peer routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a05b5-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="a05b5-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="a05b5-119">-PeerName</span></span>
<span data-ttu-id="a05b5-120">Nazwa węzła równorzędnego routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="a05b5-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="a05b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="a05b5-122">Nazwa grupy zasobów równorzędnych routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="a05b5-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="a05b5-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="a05b5-123">-VirtualRouterName</span></span>
<span data-ttu-id="a05b5-124">Nazwa routera wirtualnego</span><span class="sxs-lookup"><span data-stu-id="a05b5-124">Virtual router name</span></span>

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

### <span data-ttu-id="a05b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05b5-125">CommonParameters</span></span>
<span data-ttu-id="a05b5-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a05b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05b5-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a05b5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05b5-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a05b5-128">INPUTS</span></span>

### <span data-ttu-id="a05b5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a05b5-129">System.String</span></span>

### <span data-ttu-id="a05b5-130">Microsoft. Azure. Commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="a05b5-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="a05b5-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a05b5-131">OUTPUTS</span></span>

### <span data-ttu-id="a05b5-132">Microsoft. Azure. Commands. Network. models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="a05b5-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="a05b5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a05b5-133">NOTES</span></span>

## <span data-ttu-id="a05b5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a05b5-134">RELATED LINKS</span></span>

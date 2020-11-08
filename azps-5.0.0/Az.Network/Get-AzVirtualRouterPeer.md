---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225869"
---
# <span data-ttu-id="cd72e-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cd72e-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="cd72e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd72e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd72e-103">Pobiera VirtualRouter peer na platformie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cd72e-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="cd72e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd72e-104">SYNTAX</span></span>

### <span data-ttu-id="cd72e-105">VirtualRouterPeerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd72e-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd72e-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd72e-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd72e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd72e-107">DESCRIPTION</span></span>
<span data-ttu-id="cd72e-108">Polecenie cmdlet **Get-AzVirtualRouterPeer** Pobiera element równorzędny na platformie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cd72e-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="cd72e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd72e-109">EXAMPLES</span></span>

### <span data-ttu-id="cd72e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd72e-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="cd72e-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cd72e-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="cd72e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd72e-112">PARAMETERS</span></span>

### <span data-ttu-id="cd72e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd72e-113">-DefaultProfile</span></span>
<span data-ttu-id="cd72e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd72e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd72e-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="cd72e-115">-PeerName</span></span>
<span data-ttu-id="cd72e-116">Nazwa węzła równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="cd72e-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="cd72e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd72e-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd72e-118">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="cd72e-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="cd72e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd72e-119">-ResourceId</span></span>
<span data-ttu-id="cd72e-120">Identyfikator zasobu routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="cd72e-120">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd72e-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="cd72e-121">-VirtualRouterName</span></span>
<span data-ttu-id="cd72e-122">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="cd72e-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="cd72e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd72e-123">CommonParameters</span></span>
<span data-ttu-id="cd72e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd72e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd72e-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd72e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd72e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd72e-126">INPUTS</span></span>

### <span data-ttu-id="cd72e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cd72e-127">System.String</span></span>

## <span data-ttu-id="cd72e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd72e-128">OUTPUTS</span></span>

### <span data-ttu-id="cd72e-129">Microsoft. Azure. Commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cd72e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="cd72e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd72e-130">NOTES</span></span>

## <span data-ttu-id="cd72e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd72e-131">RELATED LINKS</span></span>

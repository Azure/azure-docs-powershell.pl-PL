---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: cf662dcd74182776131a5b7cfe3df3d86d20c14b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050328"
---
# <span data-ttu-id="7577b-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="7577b-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="7577b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7577b-102">SYNOPSIS</span></span>
<span data-ttu-id="7577b-103">Pobiera VirtualRouter peer na platformie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="7577b-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>


## <span data-ttu-id="7577b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7577b-104">SYNTAX</span></span>

### <span data-ttu-id="7577b-105">VirtualRouterPeerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7577b-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7577b-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7577b-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7577b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7577b-107">DESCRIPTION</span></span>
<span data-ttu-id="7577b-108">Polecenie cmdlet **Get-AzVirtualRouterPeer** Pobiera element równorzędny na platformie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="7577b-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="7577b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7577b-109">EXAMPLES</span></span>

### <span data-ttu-id="7577b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7577b-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -RouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="7577b-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7577b-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="7577b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7577b-112">PARAMETERS</span></span>

### <span data-ttu-id="7577b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7577b-113">-DefaultProfile</span></span>
<span data-ttu-id="7577b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7577b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7577b-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="7577b-115">-PeerName</span></span>
<span data-ttu-id="7577b-116">Nazwa węzła równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="7577b-116">The name of the virtual router peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7577b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7577b-117">-ResourceGroupName</span></span>
<span data-ttu-id="7577b-118">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="7577b-118">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7577b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7577b-119">-ResourceId</span></span>
<span data-ttu-id="7577b-120">Identyfikator zasobu routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="7577b-120">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7577b-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="7577b-121">-VirtualRouterName</span></span>
<span data-ttu-id="7577b-122">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="7577b-122">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7577b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7577b-123">CommonParameters</span></span>
<span data-ttu-id="7577b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7577b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7577b-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7577b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7577b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7577b-126">INPUTS</span></span>

### <span data-ttu-id="7577b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7577b-127">System.String</span></span>

## <span data-ttu-id="7577b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7577b-128">OUTPUTS</span></span>

### <span data-ttu-id="7577b-129">Microsoft. Azure. Commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="7577b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="7577b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7577b-130">NOTES</span></span>

## <span data-ttu-id="7577b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7577b-131">RELATED LINKS</span></span>

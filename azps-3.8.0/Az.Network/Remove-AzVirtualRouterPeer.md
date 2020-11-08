---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 871a06a2bbd3a844dd758dbc16189afdb261db2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052931"
---
# <span data-ttu-id="954eb-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="954eb-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="954eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="954eb-102">SYNOPSIS</span></span>
<span data-ttu-id="954eb-103">Usuwa węzeł równorzędny z usługi Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="954eb-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="954eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="954eb-104">SYNTAX</span></span>

### <span data-ttu-id="954eb-105">VirtualRouterPeerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="954eb-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="954eb-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="954eb-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="954eb-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="954eb-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="954eb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="954eb-108">DESCRIPTION</span></span>
<span data-ttu-id="954eb-109">Polecenie cmdlet **Remove-AzVirtualRouterPeer** usuwa VirtualRouter peer z usługi Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="954eb-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="954eb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="954eb-110">EXAMPLES</span></span>

### <span data-ttu-id="954eb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="954eb-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="954eb-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="954eb-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="954eb-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="954eb-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="954eb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="954eb-114">PARAMETERS</span></span>

### <span data-ttu-id="954eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="954eb-115">-AsJob</span></span>
<span data-ttu-id="954eb-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="954eb-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954eb-117">-DefaultProfile</span></span>
<span data-ttu-id="954eb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="954eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="954eb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="954eb-119">-Force</span></span>
<span data-ttu-id="954eb-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="954eb-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954eb-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="954eb-121">-InputObject</span></span>
<span data-ttu-id="954eb-122">Obiekt wejściowy peer routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="954eb-122">The virtual router peer input object.</span></span>

```yaml
Type: PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="954eb-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="954eb-123">-PeerName</span></span>
<span data-ttu-id="954eb-124">Nazwa węzła równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="954eb-124">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="954eb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="954eb-125">-ResourceGroupName</span></span>
<span data-ttu-id="954eb-126">Nazwa grupy zasobów wirtualnego routera/elementu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="954eb-126">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet, VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="954eb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="954eb-127">-ResourceId</span></span>
<span data-ttu-id="954eb-128">Identyfikator zasobu równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="954eb-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="954eb-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="954eb-129">-VirtualRouterName</span></span>
<span data-ttu-id="954eb-130">Router wirtualny, na którym znajduje się element równorzędny.</span><span class="sxs-lookup"><span data-stu-id="954eb-130">The virtual router where peer exists.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet, VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="954eb-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="954eb-131">-Confirm</span></span>
<span data-ttu-id="954eb-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="954eb-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954eb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="954eb-133">-WhatIf</span></span>
<span data-ttu-id="954eb-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="954eb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="954eb-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="954eb-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="954eb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954eb-136">CommonParameters</span></span>
<span data-ttu-id="954eb-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="954eb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954eb-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="954eb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954eb-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="954eb-139">INPUTS</span></span>

### <span data-ttu-id="954eb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="954eb-140">System.String</span></span>

### <span data-ttu-id="954eb-141">Microsoft. Azure. Commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="954eb-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="954eb-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="954eb-142">OUTPUTS</span></span>

### <span data-ttu-id="954eb-143">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="954eb-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="954eb-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="954eb-144">NOTES</span></span>

## <span data-ttu-id="954eb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="954eb-145">RELATED LINKS</span></span>

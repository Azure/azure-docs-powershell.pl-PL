---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 8d7bbf361ee2fc2bf06e1bf3ce6a9bfe1e295338
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896606"
---
# <span data-ttu-id="cdee8-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cdee8-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="cdee8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdee8-102">SYNOPSIS</span></span>
<span data-ttu-id="cdee8-103">Aktualizowanie elementu równorzędnego w usłudze Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cdee8-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="cdee8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdee8-104">SYNTAX</span></span>

### <span data-ttu-id="cdee8-105">VirtualRouterNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cdee8-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdee8-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdee8-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdee8-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdee8-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdee8-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdee8-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdee8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cdee8-109">DESCRIPTION</span></span>
<span data-ttu-id="cdee8-110">Polecenie cmdlet **Update-AzVirtualRouterPeer** powoduje zaktualizowanie elementu równorzędnego VirtualRouter na platformie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cdee8-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="cdee8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdee8-111">EXAMPLES</span></span>

### <span data-ttu-id="cdee8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdee8-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="cdee8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cdee8-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="cdee8-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cdee8-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="cdee8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdee8-115">PARAMETERS</span></span>

### <span data-ttu-id="cdee8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdee8-116">-AsJob</span></span>
<span data-ttu-id="cdee8-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cdee8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdee8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdee8-118">-DefaultProfile</span></span>
<span data-ttu-id="cdee8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdee8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdee8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cdee8-120">-Force</span></span>
<span data-ttu-id="cdee8-121">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="cdee8-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cdee8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cdee8-122">-InputObject</span></span>
<span data-ttu-id="cdee8-123">Obiekt wejściowy peer routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="cdee8-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="cdee8-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="cdee8-124">-PeerAsn</span></span>
<span data-ttu-id="cdee8-125">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="cdee8-125">Peer ASN.</span></span>

```yaml
Type: UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdee8-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="cdee8-126">-PeerIp</span></span>
<span data-ttu-id="cdee8-127">Adres IP elementu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="cdee8-127">Peer Ip.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdee8-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="cdee8-128">-PeerName</span></span>
<span data-ttu-id="cdee8-129">Nazwa węzła równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="cdee8-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="cdee8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdee8-130">-ResourceGroupName</span></span>
<span data-ttu-id="cdee8-131">Nazwa grupy zasobów wirtualnego routera/elementu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="cdee8-131">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdee8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdee8-132">-ResourceId</span></span>
<span data-ttu-id="cdee8-133">Identyfikator zasobu równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="cdee8-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="cdee8-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="cdee8-134">-VirtualRouterName</span></span>
<span data-ttu-id="cdee8-135">Router wirtualny, na którym znajduje się element równorzędny.</span><span class="sxs-lookup"><span data-stu-id="cdee8-135">The virtual router where peer exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdee8-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdee8-136">-Confirm</span></span>
<span data-ttu-id="cdee8-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdee8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdee8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdee8-138">-WhatIf</span></span>
<span data-ttu-id="cdee8-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdee8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdee8-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cdee8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdee8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdee8-141">CommonParameters</span></span>
<span data-ttu-id="cdee8-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdee8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdee8-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdee8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdee8-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdee8-144">INPUTS</span></span>

### <span data-ttu-id="cdee8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cdee8-145">System.String</span></span>

### <span data-ttu-id="cdee8-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="cdee8-146">System.UInt32</span></span>

### <span data-ttu-id="cdee8-147">Microsoft. Azure. Commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cdee8-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="cdee8-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdee8-148">OUTPUTS</span></span>

### <span data-ttu-id="cdee8-149">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cdee8-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="cdee8-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdee8-150">NOTES</span></span>

## <span data-ttu-id="cdee8-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdee8-151">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 9e82946d13ac830d50affc621c965cfe8b81c503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951482"
---
# <span data-ttu-id="63460-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="63460-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="63460-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63460-102">SYNOPSIS</span></span>
<span data-ttu-id="63460-103">Aktualizowanie elementu równorzędnego w programie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="63460-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="63460-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="63460-104">SYNTAX</span></span>

### <span data-ttu-id="63460-105">VirtualRouterNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="63460-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63460-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63460-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63460-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63460-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63460-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63460-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63460-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="63460-109">DESCRIPTION</span></span>
<span data-ttu-id="63460-110">Polecenie **cmdlet Update-AzVirtualRouterPeer** aktualizuje element równorzędny VirtualRouter na platformie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="63460-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="63460-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="63460-111">EXAMPLES</span></span>

### <span data-ttu-id="63460-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63460-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="63460-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="63460-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="63460-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="63460-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="63460-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63460-115">PARAMETERS</span></span>

### <span data-ttu-id="63460-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="63460-116">-AsJob</span></span>
<span data-ttu-id="63460-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="63460-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63460-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63460-118">-DefaultProfile</span></span>
<span data-ttu-id="63460-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="63460-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63460-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="63460-120">-Force</span></span>
<span data-ttu-id="63460-121">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="63460-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="63460-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63460-122">-InputObject</span></span>
<span data-ttu-id="63460-123">Obiekt wejściowy równorzędny routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="63460-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="63460-124">- PeerAsn</span><span class="sxs-lookup"><span data-stu-id="63460-124">-PeerAsn</span></span>
<span data-ttu-id="63460-125">Równorzędna asn.</span><span class="sxs-lookup"><span data-stu-id="63460-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63460-126">— Komunikacja równorzędna</span><span class="sxs-lookup"><span data-stu-id="63460-126">-PeerIp</span></span>
<span data-ttu-id="63460-127">Adres IP współpracownika.</span><span class="sxs-lookup"><span data-stu-id="63460-127">Peer Ip.</span></span>

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

### <span data-ttu-id="63460-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="63460-128">-PeerName</span></span>
<span data-ttu-id="63460-129">Nazwa komputera równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="63460-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="63460-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63460-130">-ResourceGroupName</span></span>
<span data-ttu-id="63460-131">Nazwa grupy zasobów routera/elementu równorzędnego wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="63460-131">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63460-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63460-132">-ResourceId</span></span>
<span data-ttu-id="63460-133">Identyfikator zasobu równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="63460-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="63460-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="63460-134">-VirtualRouterName</span></span>
<span data-ttu-id="63460-135">Router wirtualny, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="63460-135">The virtual router where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63460-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63460-136">-Confirm</span></span>
<span data-ttu-id="63460-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="63460-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63460-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63460-138">-WhatIf</span></span>
<span data-ttu-id="63460-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63460-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63460-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="63460-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63460-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63460-141">CommonParameters</span></span>
<span data-ttu-id="63460-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63460-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63460-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63460-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63460-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63460-144">INPUTS</span></span>

### <span data-ttu-id="63460-145">System.String</span><span class="sxs-lookup"><span data-stu-id="63460-145">System.String</span></span>

### <span data-ttu-id="63460-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="63460-146">System.UInt32</span></span>

### <span data-ttu-id="63460-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="63460-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="63460-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63460-148">OUTPUTS</span></span>

### <span data-ttu-id="63460-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="63460-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="63460-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="63460-150">NOTES</span></span>

## <span data-ttu-id="63460-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63460-151">RELATED LINKS</span></span>

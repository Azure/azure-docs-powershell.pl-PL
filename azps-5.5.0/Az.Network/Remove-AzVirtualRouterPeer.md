---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240610"
---
# <span data-ttu-id="2556b-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2556b-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="2556b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2556b-102">SYNOPSIS</span></span>
<span data-ttu-id="2556b-103">Usuwa element równorzędny z wirtualnego przekierowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2556b-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="2556b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2556b-104">SYNTAX</span></span>

### <span data-ttu-id="2556b-105">VirtualRouterPeerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2556b-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2556b-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2556b-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2556b-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2556b-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2556b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2556b-108">DESCRIPTION</span></span>
<span data-ttu-id="2556b-109">Polecenie **cmdlet Remove-AzVirtualRouterPeer** usuwa element równorzędny VirtualRouter z wirtualnego przekierowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2556b-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="2556b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2556b-110">EXAMPLES</span></span>

### <span data-ttu-id="2556b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2556b-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="2556b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2556b-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="2556b-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2556b-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="2556b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2556b-114">PARAMETERS</span></span>

### <span data-ttu-id="2556b-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2556b-115">-AsJob</span></span>
<span data-ttu-id="2556b-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2556b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2556b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2556b-117">-DefaultProfile</span></span>
<span data-ttu-id="2556b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2556b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2556b-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2556b-119">-Force</span></span>
<span data-ttu-id="2556b-120">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="2556b-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2556b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2556b-121">-InputObject</span></span>
<span data-ttu-id="2556b-122">Obiekt wejściowy równorzędny routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="2556b-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="2556b-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2556b-123">-PeerName</span></span>
<span data-ttu-id="2556b-124">Nazwa komputera równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="2556b-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="2556b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2556b-125">-ResourceGroupName</span></span>
<span data-ttu-id="2556b-126">Nazwa grupy zasobów routera/elementu równorzędnego wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="2556b-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="2556b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2556b-127">-ResourceId</span></span>
<span data-ttu-id="2556b-128">Identyfikator zasobu równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="2556b-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="2556b-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="2556b-129">-VirtualRouterName</span></span>
<span data-ttu-id="2556b-130">Router wirtualny, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="2556b-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="2556b-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2556b-131">-Confirm</span></span>
<span data-ttu-id="2556b-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2556b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2556b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2556b-133">-WhatIf</span></span>
<span data-ttu-id="2556b-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2556b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2556b-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2556b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2556b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2556b-136">CommonParameters</span></span>
<span data-ttu-id="2556b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2556b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2556b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2556b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2556b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2556b-139">INPUTS</span></span>

### <span data-ttu-id="2556b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2556b-140">System.String</span></span>

### <span data-ttu-id="2556b-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2556b-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="2556b-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2556b-142">OUTPUTS</span></span>

### <span data-ttu-id="2556b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2556b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="2556b-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2556b-144">NOTES</span></span>

## <span data-ttu-id="2556b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2556b-145">RELATED LINKS</span></span>

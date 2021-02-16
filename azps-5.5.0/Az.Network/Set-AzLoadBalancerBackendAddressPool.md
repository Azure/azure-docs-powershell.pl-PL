---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186867"
---
# <span data-ttu-id="9c5e3-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c5e3-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="9c5e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5e3-103">Aktualizuje pulę zaplecza w równoważeniu obciążenia</span><span class="sxs-lookup"><span data-stu-id="9c5e3-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="9c5e3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c5e3-104">SYNTAX</span></span>

### <span data-ttu-id="9c5e3-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c5e3-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c5e3-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c5e3-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c5e3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c5e3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c5e3-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c5e3-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c5e3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c5e3-109">DESCRIPTION</span></span>
<span data-ttu-id="9c5e3-110">Aktualizuje pulę zaplecza dla równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9c5e3-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="9c5e3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c5e3-111">EXAMPLES</span></span>

### <span data-ttu-id="9c5e3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c5e3-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="9c5e3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9c5e3-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="9c5e3-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9c5e3-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="9c5e3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c5e3-115">PARAMETERS</span></span>

### <span data-ttu-id="9c5e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5e3-116">-DefaultProfile</span></span>
<span data-ttu-id="9c5e3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c5e3-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9c5e3-118">-Force</span></span>
<span data-ttu-id="9c5e3-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9c5e3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c5e3-120">-InputObject</span></span>
<span data-ttu-id="9c5e3-121">Pula adresów zaplecza do ustawienia</span><span class="sxs-lookup"><span data-stu-id="9c5e3-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5e3-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c5e3-122">-LoadBalancer</span></span>
<span data-ttu-id="9c5e3-123">Zasób równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5e3-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="9c5e3-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="9c5e3-125">Adresy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5e3-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="9c5e3-126">-LoadBalancerName</span></span>
<span data-ttu-id="9c5e3-127">Nazwa urządzenia do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5e3-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9c5e3-128">-Name</span></span>
<span data-ttu-id="9c5e3-129">Nazwa puli zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5e3-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c5e3-130">-PassThru</span></span>
<span data-ttu-id="9c5e3-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="9c5e3-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9c5e3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c5e3-132">-ResourceGroupName</span></span>
<span data-ttu-id="9c5e3-133">Nazwa grupy zasobów dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5e3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c5e3-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5e3-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c5e3-135">-Confirm</span></span>
<span data-ttu-id="9c5e3-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c5e3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c5e3-137">-WhatIf</span></span>
<span data-ttu-id="9c5e3-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c5e3-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c5e3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5e3-140">CommonParameters</span></span>
<span data-ttu-id="9c5e3-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5e3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5e3-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c5e3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5e3-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c5e3-143">INPUTS</span></span>

### <span data-ttu-id="9c5e3-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c5e3-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9c5e3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9c5e3-145">System.String</span></span>

## <span data-ttu-id="9c5e3-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c5e3-146">OUTPUTS</span></span>

### <span data-ttu-id="9c5e3-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9c5e3-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="9c5e3-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c5e3-148">NOTES</span></span>

## <span data-ttu-id="9c5e3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c5e3-149">RELATED LINKS</span></span>

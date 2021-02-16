---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179651"
---
# <span data-ttu-id="27410-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="27410-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="27410-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27410-102">SYNOPSIS</span></span>
<span data-ttu-id="27410-103">Tworzy pulę adresów zaplecza dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="27410-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="27410-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27410-104">SYNTAX</span></span>

### <span data-ttu-id="27410-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27410-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27410-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27410-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27410-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="27410-107">DESCRIPTION</span></span>
<span data-ttu-id="27410-108">Tworzy pulę adresów zaplecza dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="27410-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="27410-109">Umożliwia specyfikowanie tablicy PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="27410-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="27410-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27410-110">EXAMPLES</span></span>

### <span data-ttu-id="27410-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27410-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="27410-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="27410-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="27410-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="27410-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="27410-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="27410-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="27410-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27410-115">PARAMETERS</span></span>

### <span data-ttu-id="27410-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27410-116">-DefaultProfile</span></span>
<span data-ttu-id="27410-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="27410-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27410-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27410-118">-LoadBalancer</span></span>
<span data-ttu-id="27410-119">Zasób równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="27410-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27410-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="27410-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="27410-121">Adresy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="27410-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27410-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="27410-122">-LoadBalancerName</span></span>
<span data-ttu-id="27410-123">Nazwa urządzenia do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="27410-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27410-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="27410-124">-Name</span></span>
<span data-ttu-id="27410-125">Nazwa puli zaplecza.</span><span class="sxs-lookup"><span data-stu-id="27410-125">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27410-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27410-126">-ResourceGroupName</span></span>
<span data-ttu-id="27410-127">Nazwa grupy zasobów dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="27410-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27410-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27410-128">-Confirm</span></span>
<span data-ttu-id="27410-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="27410-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27410-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27410-130">-WhatIf</span></span>
<span data-ttu-id="27410-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27410-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27410-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="27410-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27410-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27410-133">CommonParameters</span></span>
<span data-ttu-id="27410-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27410-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27410-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27410-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27410-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27410-136">INPUTS</span></span>

### <span data-ttu-id="27410-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="27410-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="27410-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27410-138">OUTPUTS</span></span>

### <span data-ttu-id="27410-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="27410-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="27410-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27410-140">NOTES</span></span>

## <span data-ttu-id="27410-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27410-141">RELATED LINKS</span></span>

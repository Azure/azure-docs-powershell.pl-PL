---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385478"
---
# <span data-ttu-id="42a22-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="42a22-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="42a22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42a22-102">SYNOPSIS</span></span>
<span data-ttu-id="42a22-103">Tworzy pulę adresów zaplecza na module równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="42a22-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="42a22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42a22-104">SYNTAX</span></span>

### <span data-ttu-id="42a22-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42a22-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a22-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42a22-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42a22-107">Opis</span><span class="sxs-lookup"><span data-stu-id="42a22-107">DESCRIPTION</span></span>
<span data-ttu-id="42a22-108">Tworzy pulę adresów zaplecza na module równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="42a22-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="42a22-109">Umożliwia specifiying PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="42a22-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="42a22-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42a22-110">EXAMPLES</span></span>

### <span data-ttu-id="42a22-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42a22-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="42a22-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="42a22-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="42a22-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="42a22-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="42a22-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="42a22-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="42a22-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42a22-115">PARAMETERS</span></span>

### <span data-ttu-id="42a22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a22-116">-DefaultProfile</span></span>
<span data-ttu-id="42a22-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42a22-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42a22-118">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="42a22-118">-LoadBalancer</span></span>
<span data-ttu-id="42a22-119">Zasób modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="42a22-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="42a22-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="42a22-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="42a22-121">Adresy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="42a22-121">The backend addresses.</span></span>

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

### <span data-ttu-id="42a22-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="42a22-122">-LoadBalancerName</span></span>
<span data-ttu-id="42a22-123">Nazwa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="42a22-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="42a22-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42a22-124">-Name</span></span>
<span data-ttu-id="42a22-125">Nazwa puli wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="42a22-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="42a22-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a22-126">-ResourceGroupName</span></span>
<span data-ttu-id="42a22-127">Nazwa grupy zasobów modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="42a22-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="42a22-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42a22-128">-Confirm</span></span>
<span data-ttu-id="42a22-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42a22-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42a22-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42a22-130">-WhatIf</span></span>
<span data-ttu-id="42a22-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42a22-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42a22-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42a22-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42a22-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a22-133">CommonParameters</span></span>
<span data-ttu-id="42a22-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a22-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a22-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42a22-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a22-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42a22-136">INPUTS</span></span>

### <span data-ttu-id="42a22-137">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42a22-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="42a22-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42a22-138">OUTPUTS</span></span>

### <span data-ttu-id="42a22-139">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="42a22-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="42a22-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42a22-140">NOTES</span></span>

## <span data-ttu-id="42a22-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42a22-141">RELATED LINKS</span></span>

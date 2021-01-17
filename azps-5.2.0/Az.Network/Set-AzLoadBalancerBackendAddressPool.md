---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352801"
---
# <span data-ttu-id="de4e6-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de4e6-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="de4e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="de4e6-103">Aktualizuje pulę zaplecza na module równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="de4e6-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="de4e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de4e6-104">SYNTAX</span></span>

### <span data-ttu-id="de4e6-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="de4e6-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de4e6-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de4e6-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de4e6-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de4e6-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de4e6-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de4e6-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de4e6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="de4e6-109">DESCRIPTION</span></span>
<span data-ttu-id="de4e6-110">Aktualizuje pulę zaplecza na module równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="de4e6-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="de4e6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de4e6-111">EXAMPLES</span></span>

### <span data-ttu-id="de4e6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de4e6-112">Example 1</span></span>
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
### <span data-ttu-id="de4e6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="de4e6-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="de4e6-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="de4e6-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="de4e6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de4e6-115">PARAMETERS</span></span>

### <span data-ttu-id="de4e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4e6-116">-DefaultProfile</span></span>
<span data-ttu-id="de4e6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de4e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de4e6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="de4e6-118">-Force</span></span>
<span data-ttu-id="de4e6-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="de4e6-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="de4e6-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="de4e6-120">-InputObject</span></span>
<span data-ttu-id="de4e6-121">Pula adresów zaplecza, która ma zostać ustawiona</span><span class="sxs-lookup"><span data-stu-id="de4e6-121">The backend address pool to set</span></span>

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

### <span data-ttu-id="de4e6-122">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="de4e6-122">-LoadBalancer</span></span>
<span data-ttu-id="de4e6-123">Zasób modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="de4e6-123">The load balancer resource.</span></span>

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

### <span data-ttu-id="de4e6-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="de4e6-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="de4e6-125">Adresy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="de4e6-125">The backend addresses.</span></span>

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

### <span data-ttu-id="de4e6-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="de4e6-126">-LoadBalancerName</span></span>
<span data-ttu-id="de4e6-127">Nazwa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="de4e6-127">The name of the load balancer.</span></span>

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

### <span data-ttu-id="de4e6-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de4e6-128">-Name</span></span>
<span data-ttu-id="de4e6-129">Nazwa puli wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="de4e6-129">The name of the backend pool.</span></span>

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

### <span data-ttu-id="de4e6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de4e6-130">-PassThru</span></span>
<span data-ttu-id="de4e6-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="de4e6-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="de4e6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4e6-132">-ResourceGroupName</span></span>
<span data-ttu-id="de4e6-133">Nazwa grupy zasobów modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="de4e6-133">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="de4e6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de4e6-134">-ResourceId</span></span>

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

### <span data-ttu-id="de4e6-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de4e6-135">-Confirm</span></span>
<span data-ttu-id="de4e6-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de4e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de4e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de4e6-137">-WhatIf</span></span>
<span data-ttu-id="de4e6-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de4e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de4e6-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de4e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de4e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4e6-140">CommonParameters</span></span>
<span data-ttu-id="de4e6-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de4e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4e6-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de4e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4e6-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de4e6-143">INPUTS</span></span>

### <span data-ttu-id="de4e6-144">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="de4e6-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="de4e6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="de4e6-145">System.String</span></span>

## <span data-ttu-id="de4e6-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de4e6-146">OUTPUTS</span></span>

### <span data-ttu-id="de4e6-147">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de4e6-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="de4e6-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de4e6-148">NOTES</span></span>

## <span data-ttu-id="de4e6-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de4e6-149">RELATED LINKS</span></span>

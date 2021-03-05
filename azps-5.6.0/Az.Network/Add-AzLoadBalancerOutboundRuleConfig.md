---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: d59bb27608e1ccf614048dcd27eb6643695ba523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006490"
---
# <span data-ttu-id="59cd6-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59cd6-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="59cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="59cd6-103">Dodaje konfigurację reguły ruchu wychodzącego do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="59cd6-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="59cd6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59cd6-104">SYNTAX</span></span>

### <span data-ttu-id="59cd6-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="59cd6-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59cd6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="59cd6-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59cd6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="59cd6-107">DESCRIPTION</span></span>
<span data-ttu-id="59cd6-108">Polecenie **cmdlet Add-AzLoadBalancerOutboundRuleConfig** dodaje konfigurację reguły ruchu wychodzącego do narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="59cd6-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="59cd6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59cd6-109">EXAMPLES</span></span>

### <span data-ttu-id="59cd6-110">Przykład 1. Dodawanie konfiguracji reguły ruchu wychodzącego do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="59cd6-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="59cd6-111">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="59cd6-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="59cd6-112">Drugie polecenie korzysta z operatora potoku w celu przekazania równoważenia obciążenia w programie $slb do dodatku **Add-AzLoadBalancerOutboundRuleConfig,** co powoduje dodanie konfiguracji reguły ruchu wychodzącego do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="59cd6-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="59cd6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59cd6-113">PARAMETERS</span></span>

### <span data-ttu-id="59cd6-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="59cd6-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="59cd6-115">Liczba portów wychodzących, które mają być używane na pasku nat.</span><span class="sxs-lookup"><span data-stu-id="59cd6-115">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59cd6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="59cd6-116">-BackendAddressPool</span></span>
<span data-ttu-id="59cd6-117">Odwołanie do puli dipów.</span><span class="sxs-lookup"><span data-stu-id="59cd6-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="59cd6-118">Ruch wychodzący jest losowo ładowany na wielu serwerach IP w ramach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="59cd6-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59cd6-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="59cd6-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="59cd6-120">Odwołanie do puli dipów.</span><span class="sxs-lookup"><span data-stu-id="59cd6-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="59cd6-121">Ruch wychodzący jest losowo ładowany na wielu serwerach IP w ramach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="59cd6-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59cd6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59cd6-122">-DefaultProfile</span></span>
<span data-ttu-id="59cd6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59cd6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59cd6-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="59cd6-124">-EnableTcpReset</span></span>
<span data-ttu-id="59cd6-125">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="59cd6-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="59cd6-126">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="59cd6-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="59cd6-127">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="59cd6-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="59cd6-128">Adresy IP frontendu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="59cd6-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59cd6-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="59cd6-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="59cd6-130">Limit czasu dla bezczynne połączenie TCP</span><span class="sxs-lookup"><span data-stu-id="59cd6-130">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59cd6-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59cd6-131">-LoadBalancer</span></span>
<span data-ttu-id="59cd6-132">Odwołanie do zasobu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="59cd6-132">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59cd6-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="59cd6-133">-Name</span></span>
<span data-ttu-id="59cd6-134">Nazwa reguły wychodzącej.</span><span class="sxs-lookup"><span data-stu-id="59cd6-134">Name of the outbound rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59cd6-135">— Protokół</span><span class="sxs-lookup"><span data-stu-id="59cd6-135">-Protocol</span></span>
<span data-ttu-id="59cd6-136">Protokół — TCP, UDP lub All</span><span class="sxs-lookup"><span data-stu-id="59cd6-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="59cd6-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59cd6-137">-Confirm</span></span>
<span data-ttu-id="59cd6-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59cd6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59cd6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59cd6-139">-WhatIf</span></span>
<span data-ttu-id="59cd6-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59cd6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59cd6-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="59cd6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59cd6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59cd6-142">CommonParameters</span></span>
<span data-ttu-id="59cd6-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59cd6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59cd6-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59cd6-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59cd6-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59cd6-145">INPUTS</span></span>

### <span data-ttu-id="59cd6-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59cd6-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="59cd6-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="59cd6-147">System.Int32</span></span>

### <span data-ttu-id="59cd6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="59cd6-148">System.String</span></span>

### <span data-ttu-id="59cd6-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="59cd6-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="59cd6-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="59cd6-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="59cd6-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59cd6-151">OUTPUTS</span></span>

### <span data-ttu-id="59cd6-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59cd6-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="59cd6-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59cd6-153">NOTES</span></span>

## <span data-ttu-id="59cd6-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59cd6-154">RELATED LINKS</span></span>

[<span data-ttu-id="59cd6-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59cd6-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="59cd6-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59cd6-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="59cd6-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59cd6-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="59cd6-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59cd6-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)

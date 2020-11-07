---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 79a8442d28d6e04d4e6e013e536663a19faaf3f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709671"
---
# <span data-ttu-id="c8bbb-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8bbb-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c8bbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bbb-103">Umożliwia dodanie konfiguracji reguły wychodzącej do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="c8bbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8bbb-104">SYNTAX</span></span>

### <span data-ttu-id="c8bbb-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c8bbb-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8bbb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c8bbb-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8bbb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c8bbb-107">DESCRIPTION</span></span>
<span data-ttu-id="c8bbb-108">Polecenie cmdlet **Add-AzLoadBalancerOutboundRuleConfig** umożliwia dodanie konfiguracji reguły wychodzącej do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c8bbb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8bbb-109">EXAMPLES</span></span>

### <span data-ttu-id="c8bbb-110">Przykład 1: Dodawanie konfiguracji reguły ruchu wychodzącego do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c8bbb-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="c8bbb-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c8bbb-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzLoadBalancerOutboundRuleConfig** , które powoduje dodanie konfiguracji reguły ruchu wychodzącego do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="c8bbb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8bbb-113">PARAMETERS</span></span>

### <span data-ttu-id="c8bbb-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="c8bbb-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="c8bbb-115">Liczba portów wychodzących, które mają być używane do obsługi translatora adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="c8bbb-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c8bbb-116">-BackendAddressPool</span></span>
<span data-ttu-id="c8bbb-117">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c8bbb-118">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c8bbb-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c8bbb-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="c8bbb-120">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c8bbb-121">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c8bbb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bbb-122">-DefaultProfile</span></span>
<span data-ttu-id="c8bbb-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8bbb-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c8bbb-124">-EnableTcpReset</span></span>
<span data-ttu-id="c8bbb-125">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="c8bbb-126">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c8bbb-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8bbb-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c8bbb-128">Adresy IP frontonu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="c8bbb-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c8bbb-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c8bbb-130">Limit czasu bezczynności połączenia TCP</span><span class="sxs-lookup"><span data-stu-id="c8bbb-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="c8bbb-131">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c8bbb-131">-LoadBalancer</span></span>
<span data-ttu-id="c8bbb-132">Odwołanie do zasobu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="c8bbb-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8bbb-133">-Name</span></span>
<span data-ttu-id="c8bbb-134">Nazwa reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c8bbb-135">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="c8bbb-135">-Protocol</span></span>
<span data-ttu-id="c8bbb-136">Protocol-TCP, UDP lub All</span><span class="sxs-lookup"><span data-stu-id="c8bbb-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="c8bbb-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8bbb-137">-Confirm</span></span>
<span data-ttu-id="c8bbb-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8bbb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8bbb-139">-WhatIf</span></span>
<span data-ttu-id="c8bbb-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8bbb-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8bbb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bbb-142">CommonParameters</span></span>
<span data-ttu-id="c8bbb-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8bbb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bbb-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8bbb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bbb-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8bbb-145">INPUTS</span></span>

### <span data-ttu-id="c8bbb-146">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c8bbb-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c8bbb-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c8bbb-147">System.Int32</span></span>

### <span data-ttu-id="c8bbb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c8bbb-148">System.String</span></span>

### <span data-ttu-id="c8bbb-149">Microsoft. Azure. Commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="c8bbb-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="c8bbb-150">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c8bbb-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c8bbb-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8bbb-151">OUTPUTS</span></span>

### <span data-ttu-id="c8bbb-152">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c8bbb-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c8bbb-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8bbb-153">NOTES</span></span>

## <span data-ttu-id="c8bbb-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8bbb-154">RELATED LINKS</span></span>

[<span data-ttu-id="c8bbb-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8bbb-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c8bbb-156">Nowe — AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8bbb-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c8bbb-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8bbb-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c8bbb-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8bbb-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)

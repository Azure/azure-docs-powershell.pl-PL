---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049997"
---
# <span data-ttu-id="58b4f-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58b4f-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="58b4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="58b4f-103">Umożliwia dodanie konfiguracji reguły wychodzącej do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="58b4f-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="58b4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58b4f-104">SYNTAX</span></span>

### <span data-ttu-id="58b4f-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="58b4f-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58b4f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58b4f-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="58b4f-107">DESCRIPTION</span></span>
<span data-ttu-id="58b4f-108">Polecenie cmdlet **Add-AzLoadBalancerOutboundRuleConfig** umożliwia dodanie konfiguracji reguły wychodzącej do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="58b4f-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="58b4f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58b4f-109">EXAMPLES</span></span>

### <span data-ttu-id="58b4f-110">Przykład 1: Dodawanie konfiguracji reguły ruchu wychodzącego do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="58b4f-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="58b4f-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="58b4f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="58b4f-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzLoadBalancerOutboundRuleConfig** , które powoduje dodanie konfiguracji reguły ruchu wychodzącego do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="58b4f-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="58b4f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58b4f-113">PARAMETERS</span></span>

### <span data-ttu-id="58b4f-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="58b4f-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="58b4f-115">Liczba portów wychodzących, które mają być używane do obsługi translatora adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="58b4f-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="58b4f-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58b4f-116">-BackendAddressPool</span></span>
<span data-ttu-id="58b4f-117">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="58b4f-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="58b4f-118">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="58b4f-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="58b4f-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="58b4f-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="58b4f-120">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="58b4f-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="58b4f-121">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="58b4f-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="58b4f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b4f-122">-DefaultProfile</span></span>
<span data-ttu-id="58b4f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58b4f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58b4f-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="58b4f-124">-EnableTcpReset</span></span>
<span data-ttu-id="58b4f-125">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="58b4f-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="58b4f-126">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="58b4f-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="58b4f-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="58b4f-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="58b4f-128">Adresy IP frontonu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="58b4f-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="58b4f-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="58b4f-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="58b4f-130">Limit czasu bezczynności połączenia TCP</span><span class="sxs-lookup"><span data-stu-id="58b4f-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="58b4f-131">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="58b4f-131">-LoadBalancer</span></span>
<span data-ttu-id="58b4f-132">Odwołanie do zasobu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="58b4f-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="58b4f-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58b4f-133">-Name</span></span>
<span data-ttu-id="58b4f-134">Nazwa reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="58b4f-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="58b4f-135">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="58b4f-135">-Protocol</span></span>
<span data-ttu-id="58b4f-136">Protocol-TCP, UDP lub All</span><span class="sxs-lookup"><span data-stu-id="58b4f-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="58b4f-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58b4f-137">-Confirm</span></span>
<span data-ttu-id="58b4f-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58b4f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b4f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b4f-139">-WhatIf</span></span>
<span data-ttu-id="58b4f-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58b4f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58b4f-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58b4f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b4f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b4f-142">CommonParameters</span></span>
<span data-ttu-id="58b4f-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b4f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b4f-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b4f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b4f-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58b4f-145">INPUTS</span></span>

### <span data-ttu-id="58b4f-146">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58b4f-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="58b4f-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="58b4f-147">System.Int32</span></span>

### <span data-ttu-id="58b4f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="58b4f-148">System.String</span></span>

### <span data-ttu-id="58b4f-149">Microsoft. Azure. Commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="58b4f-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="58b4f-150">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58b4f-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="58b4f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58b4f-151">OUTPUTS</span></span>

### <span data-ttu-id="58b4f-152">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58b4f-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="58b4f-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58b4f-153">NOTES</span></span>

## <span data-ttu-id="58b4f-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58b4f-154">RELATED LINKS</span></span>

[<span data-ttu-id="58b4f-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58b4f-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="58b4f-156">Nowe — AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58b4f-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="58b4f-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58b4f-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="58b4f-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58b4f-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)

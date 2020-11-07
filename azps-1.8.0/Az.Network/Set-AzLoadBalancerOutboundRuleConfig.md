---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 482f729f0ee3fa3efc6a78a1bc2b5fbbd3fe1d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708969"
---
# <span data-ttu-id="187c5-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="187c5-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="187c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="187c5-102">SYNOPSIS</span></span>
<span data-ttu-id="187c5-103">Ustawia konfigurację reguły ruchu wychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="187c5-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="187c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="187c5-104">SYNTAX</span></span>

### <span data-ttu-id="187c5-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="187c5-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187c5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="187c5-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="187c5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="187c5-107">DESCRIPTION</span></span>
<span data-ttu-id="187c5-108">Polecenie cmdlet **Set-AzLoadBalancerOutboundRuleConfig** ustawia konfigurację reguły ruchu wychodzącego dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="187c5-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="187c5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="187c5-109">EXAMPLES</span></span>

### <span data-ttu-id="187c5-110">Przykład 1. modyfikowanie konfiguracji reguły ruchu wychodzącego w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="187c5-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="187c5-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="187c5-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="187c5-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerOutboundRuleConfig, które umożliwia dodanie do niego konfiguracji reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="187c5-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="187c5-113">Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzLoadBalancerOutboundRuleConfig** , co umożliwia zapisanie i zaktualizowanie konfiguracji reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="187c5-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="187c5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="187c5-114">PARAMETERS</span></span>

### <span data-ttu-id="187c5-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="187c5-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="187c5-116">Liczba portów wychodzących, które mają być używane do obsługi translatora adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="187c5-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="187c5-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="187c5-117">-BackendAddressPool</span></span>
<span data-ttu-id="187c5-118">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="187c5-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="187c5-119">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="187c5-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="187c5-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="187c5-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="187c5-121">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="187c5-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="187c5-122">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="187c5-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="187c5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187c5-123">-DefaultProfile</span></span>
<span data-ttu-id="187c5-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="187c5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="187c5-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="187c5-125">-EnableTcpReset</span></span>
<span data-ttu-id="187c5-126">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="187c5-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="187c5-127">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="187c5-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="187c5-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="187c5-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="187c5-129">Adresy IP frontonu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="187c5-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="187c5-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="187c5-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="187c5-131">Limit czasu bezczynności połączenia TCP</span><span class="sxs-lookup"><span data-stu-id="187c5-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="187c5-132">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="187c5-132">-LoadBalancer</span></span>
<span data-ttu-id="187c5-133">Odwołanie do zasobu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="187c5-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="187c5-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="187c5-134">-Name</span></span>
<span data-ttu-id="187c5-135">Nazwa reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="187c5-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="187c5-136">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="187c5-136">-Protocol</span></span>
<span data-ttu-id="187c5-137">Protocol-TCP, UDP lub All</span><span class="sxs-lookup"><span data-stu-id="187c5-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="187c5-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="187c5-138">-Confirm</span></span>
<span data-ttu-id="187c5-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="187c5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="187c5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187c5-140">-WhatIf</span></span>
<span data-ttu-id="187c5-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="187c5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="187c5-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="187c5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="187c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187c5-143">CommonParameters</span></span>
<span data-ttu-id="187c5-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="187c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187c5-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187c5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187c5-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="187c5-146">INPUTS</span></span>

### <span data-ttu-id="187c5-147">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="187c5-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="187c5-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="187c5-148">System.Int32</span></span>

### <span data-ttu-id="187c5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="187c5-149">System.String</span></span>

### <span data-ttu-id="187c5-150">Microsoft. Azure. Commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="187c5-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="187c5-151">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="187c5-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="187c5-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="187c5-152">OUTPUTS</span></span>

### <span data-ttu-id="187c5-153">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="187c5-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="187c5-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="187c5-154">NOTES</span></span>

## <span data-ttu-id="187c5-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="187c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="187c5-156">Dodaj-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="187c5-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="187c5-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="187c5-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="187c5-158">Nowe — AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="187c5-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="187c5-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="187c5-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

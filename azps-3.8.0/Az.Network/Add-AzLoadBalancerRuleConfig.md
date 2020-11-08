---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052565"
---
# <span data-ttu-id="93018-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93018-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="93018-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93018-102">SYNOPSIS</span></span>
<span data-ttu-id="93018-103">Umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="93018-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93018-104">SYNTAX</span></span>

### <span data-ttu-id="93018-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="93018-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93018-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="93018-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93018-107">Opis</span><span class="sxs-lookup"><span data-stu-id="93018-107">DESCRIPTION</span></span>
<span data-ttu-id="93018-108">Polecenie cmdlet **Add-AzLoadBalancerRuleConfig** umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="93018-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="93018-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93018-109">EXAMPLES</span></span>

### <span data-ttu-id="93018-110">Przykład 1. Dodawanie konfiguracji reguły do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="93018-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="93018-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="93018-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="93018-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzLoadBalancerRuleConfig** , które dodaje konfigurację reguły o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="93018-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="93018-113">Trzecie polecenie zaktualizuje moduł równoważenia obciążenia na platformie Azure za pomocą nowej konfiguracji reguł modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="93018-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93018-114">PARAMETERS</span></span>

### <span data-ttu-id="93018-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93018-115">-BackendAddressPool</span></span>
<span data-ttu-id="93018-116">Określa pulę adresów zaplecza, która ma zostać skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93018-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="93018-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="93018-118">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93018-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="93018-119">-BackendPort</span></span>
<span data-ttu-id="93018-120">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="93018-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93018-121">-DefaultProfile</span></span>
<span data-ttu-id="93018-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93018-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93018-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="93018-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="93018-124">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="93018-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="93018-125">-EnableFloatingIP</span></span>
<span data-ttu-id="93018-126">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="93018-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="93018-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="93018-127">-EnableTcpReset</span></span>
<span data-ttu-id="93018-128">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="93018-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="93018-129">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="93018-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="93018-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="93018-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="93018-131">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93018-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="93018-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="93018-133">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="93018-133">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93018-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="93018-134">-FrontendPort</span></span>
<span data-ttu-id="93018-135">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="93018-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="93018-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="93018-137">Określa długość czasu (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="93018-138">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="93018-138">-LoadBalancer</span></span>
<span data-ttu-id="93018-139">Określa obiekt **modułu równoważenia obciążenia** .</span><span class="sxs-lookup"><span data-stu-id="93018-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="93018-140">To polecenie cmdlet umożliwia dodanie konfiguracji reguły do modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="93018-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="93018-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="93018-141">-LoadDistribution</span></span>
<span data-ttu-id="93018-142">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-142">Specifies a load distribution.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93018-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93018-143">-Name</span></span>
<span data-ttu-id="93018-144">Określa nazwę konfiguracji reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="93018-145">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="93018-145">-Probe</span></span>
<span data-ttu-id="93018-146">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93018-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="93018-147">-ProbeId</span></span>
<span data-ttu-id="93018-148">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93018-149">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="93018-149">-Protocol</span></span>
<span data-ttu-id="93018-150">Określa protokół zgodny z regułą modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="93018-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="93018-151">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="93018-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93018-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93018-152">-Confirm</span></span>
<span data-ttu-id="93018-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93018-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93018-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93018-154">-WhatIf</span></span>
<span data-ttu-id="93018-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93018-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93018-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="93018-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93018-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93018-157">CommonParameters</span></span>
<span data-ttu-id="93018-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93018-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93018-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93018-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93018-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93018-160">INPUTS</span></span>

### <span data-ttu-id="93018-161">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="93018-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="93018-162">System. String</span><span class="sxs-lookup"><span data-stu-id="93018-162">System.String</span></span>

### <span data-ttu-id="93018-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="93018-163">System.Int32</span></span>

### <span data-ttu-id="93018-164">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="93018-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="93018-165">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93018-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="93018-166">Microsoft. Azure. Commands. Network. models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="93018-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="93018-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93018-167">OUTPUTS</span></span>

### <span data-ttu-id="93018-168">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="93018-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="93018-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93018-169">NOTES</span></span>

## <span data-ttu-id="93018-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93018-170">RELATED LINKS</span></span>

[<span data-ttu-id="93018-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="93018-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="93018-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93018-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="93018-173">Nowe — AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93018-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="93018-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93018-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="93018-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93018-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187259"
---
# <span data-ttu-id="b75a4-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b75a4-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="b75a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b75a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b75a4-103">Dodaje konfigurację reguły do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="b75a4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b75a4-104">SYNTAX</span></span>

### <span data-ttu-id="b75a4-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="b75a4-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75a4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b75a4-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b75a4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b75a4-107">DESCRIPTION</span></span>
<span data-ttu-id="b75a4-108">Polecenie **cmdlet Add-AzLoadBalancerRuleConfig** dodaje konfigurację reguły do narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b75a4-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b75a4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b75a4-109">EXAMPLES</span></span>

### <span data-ttu-id="b75a4-110">Przykład 1. Dodawanie konfiguracji reguły do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b75a4-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="b75a4-111">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="b75a4-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b75a4-112">Drugie polecenie używa operatora potoku do przekazania równoważenia obciążenia w programie $slb do dodatku **Add-AzLoadBalanceruleConfig,** co powoduje dodanie konfiguracji reguły o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="b75a4-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="b75a4-113">Trzecie polecenie zaktualizuje narzędzie do równoważenia obciążenia na platformie Azure za pomocą nowej konfiguracji reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="b75a4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b75a4-114">PARAMETERS</span></span>

### <span data-ttu-id="b75a4-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b75a4-115">-BackendAddressPool</span></span>
<span data-ttu-id="b75a4-116">Określa pulę adresów zaplecza do skojarzenia z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b75a4-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="b75a4-118">Określa identyfikator obiektu **BackendAddressPool,** który ma być skojarzony z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b75a4-119">-BackendPort</span></span>
<span data-ttu-id="b75a4-120">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75a4-121">-DefaultProfile</span></span>
<span data-ttu-id="b75a4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b75a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b75a4-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="b75a4-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="b75a4-124">Konfiguruje usługę SNAT dla maszyn wirtualnych w puli zaplecza w celu użycia adresu publicznegoip określonego w frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="b75a4-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b75a4-125">-EnableFloatingIP</span></span>
<span data-ttu-id="b75a4-126">Wskazuje, że to polecenie cmdlet umożliwia przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="b75a4-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b75a4-127">-EnableTcpReset</span></span>
<span data-ttu-id="b75a4-128">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b75a4-129">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="b75a4-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b75a4-130">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b75a4-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b75a4-131">Określa listę frontoronowych adresów IP do skojarzenia z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b75a4-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b75a4-133">Określa identyfikator konfiguracji frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="b75a4-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b75a4-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b75a4-134">-FrontendPort</span></span>
<span data-ttu-id="b75a4-135">Określa port frontoronu, który jest do siebie dopasowany przez konfigurację reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b75a4-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b75a4-137">Określa czas (w minutach), przez który stan konwersacji jest utrzymywany w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="b75a4-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b75a4-138">-LoadBalancer</span></span>
<span data-ttu-id="b75a4-139">Określa obiekt **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="b75a4-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b75a4-140">To polecenie cmdlet dodaje konfigurację reguły do równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b75a4-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b75a4-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="b75a4-141">-LoadDistribution</span></span>
<span data-ttu-id="b75a4-142">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="b75a4-143">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b75a4-143">-Name</span></span>
<span data-ttu-id="b75a4-144">Określa nazwę konfiguracji reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-145">— Dor.</span><span class="sxs-lookup"><span data-stu-id="b75a4-145">-Probe</span></span>
<span data-ttu-id="b75a4-146">Określa skojarzenie z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-147">- NaiwnyId</span><span class="sxs-lookup"><span data-stu-id="b75a4-147">-ProbeId</span></span>
<span data-ttu-id="b75a4-148">Określa identyfikator współpracownika, który ma skojarzyć z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b75a4-149">— Protokół</span><span class="sxs-lookup"><span data-stu-id="b75a4-149">-Protocol</span></span>
<span data-ttu-id="b75a4-150">Określa protokół, który jest do siebie dopasujony przez regułę równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b75a4-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="b75a4-151">Dopuszczalne wartości dla tego parametru to: Tcp lub Udp.</span><span class="sxs-lookup"><span data-stu-id="b75a4-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b75a4-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b75a4-152">-Confirm</span></span>
<span data-ttu-id="b75a4-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b75a4-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b75a4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b75a4-154">-WhatIf</span></span>
<span data-ttu-id="b75a4-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b75a4-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b75a4-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b75a4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b75a4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75a4-157">CommonParameters</span></span>
<span data-ttu-id="b75a4-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b75a4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75a4-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75a4-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75a4-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b75a4-160">INPUTS</span></span>

### <span data-ttu-id="b75a4-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b75a4-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b75a4-162">System.String</span><span class="sxs-lookup"><span data-stu-id="b75a4-162">System.String</span></span>

### <span data-ttu-id="b75a4-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b75a4-163">System.Int32</span></span>

### <span data-ttu-id="b75a4-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b75a4-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="b75a4-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b75a4-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="b75a4-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="b75a4-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="b75a4-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b75a4-167">OUTPUTS</span></span>

### <span data-ttu-id="b75a4-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b75a4-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b75a4-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b75a4-169">NOTES</span></span>

## <span data-ttu-id="b75a4-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b75a4-170">RELATED LINKS</span></span>

[<span data-ttu-id="b75a4-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b75a4-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b75a4-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b75a4-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b75a4-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b75a4-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b75a4-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b75a4-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b75a4-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b75a4-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)



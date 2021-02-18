---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240570"
---
# <span data-ttu-id="88beb-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88beb-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="88beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88beb-102">SYNOPSIS</span></span>
<span data-ttu-id="88beb-103">Aktualizuje konfigurację reguły dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="88beb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88beb-104">SYNTAX</span></span>

### <span data-ttu-id="88beb-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="88beb-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88beb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="88beb-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88beb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="88beb-107">DESCRIPTION</span></span>
<span data-ttu-id="88beb-108">Polecenie **cmdlet Set-AzLoadBalancerRuleConfig** aktualizuje konfigurację reguły dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="88beb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88beb-109">EXAMPLES</span></span>

### <span data-ttu-id="88beb-110">Przykład 1. Modyfikowanie konfiguracji reguły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="88beb-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="88beb-111">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennej $slb ładowania.</span><span class="sxs-lookup"><span data-stu-id="88beb-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="88beb-112">Drugie polecenie używa operatora potoku do przekazania równoważenia obciążenia w programie $slb do dodatku Add-AzLoadBalanceruleConfig, co powoduje dodanie do niego reguły o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="88beb-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="88beb-113">Trzecie polecenie przekazuje równoważenie obciążenia do ustawienia **Set-AzLoadBalancerRuleConfig,** co ustawia nową konfigurację reguły.</span><span class="sxs-lookup"><span data-stu-id="88beb-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="88beb-114">Pamiętaj, że konfiguracja nie powoduje włączenia przestawnego adresu IP, który został włączony przez poprzednie polecenie.</span><span class="sxs-lookup"><span data-stu-id="88beb-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="88beb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88beb-115">PARAMETERS</span></span>

### <span data-ttu-id="88beb-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="88beb-116">-BackendAddressPool</span></span>
<span data-ttu-id="88beb-117">Określa obiekt **BackendAddressPool** do skojarzenia z regułą równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="88beb-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="88beb-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="88beb-119">Określa identyfikator obiektu **BackendAddressPool,** który ma być skojarzony z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="88beb-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="88beb-120">-BackendPort</span></span>
<span data-ttu-id="88beb-121">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="88beb-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="88beb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88beb-122">-DefaultProfile</span></span>
<span data-ttu-id="88beb-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="88beb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88beb-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="88beb-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="88beb-125">Konfiguruje usługę SNAT dla maszyn wirtualnych w puli zaplecza w celu użycia adresu publicznegoip określonego w frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="88beb-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="88beb-126">-EnableFloatingIP</span></span>
<span data-ttu-id="88beb-127">Wskazuje, że to polecenie cmdlet umożliwia przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="88beb-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="88beb-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="88beb-128">-EnableTcpReset</span></span>
<span data-ttu-id="88beb-129">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="88beb-130">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="88beb-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="88beb-131">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="88beb-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="88beb-132">Określa listę frontoronowych adresów IP do skojarzenia z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="88beb-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="88beb-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="88beb-134">Określa identyfikator konfiguracji frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="88beb-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="88beb-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="88beb-135">-FrontendPort</span></span>
<span data-ttu-id="88beb-136">Określa port frontonie, który jest do siebie dopasowany przez konfigurację reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="88beb-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="88beb-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="88beb-138">Określa czas (w minutach), przez który stan konwersacji jest utrzymywany w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="88beb-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="88beb-139">-LoadBalancer</span></span>
<span data-ttu-id="88beb-140">Określa równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-140">Specifies a load balancer.</span></span>
<span data-ttu-id="88beb-141">To polecenie cmdlet aktualizuje konfigurację reguły dla równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="88beb-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="88beb-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="88beb-142">-LoadDistribution</span></span>
<span data-ttu-id="88beb-143">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-143">Specifies a load distribution.</span></span>
<span data-ttu-id="88beb-144">Dopuszczalne wartości dla tego parametru to: SourceIP i SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="88beb-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="88beb-145">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="88beb-145">-Name</span></span>
<span data-ttu-id="88beb-146">Określa nazwę równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="88beb-147">— Dor.</span><span class="sxs-lookup"><span data-stu-id="88beb-147">-Probe</span></span>
<span data-ttu-id="88beb-148">Określa wartość do skojarzenia z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="88beb-149">- NaiwnyId</span><span class="sxs-lookup"><span data-stu-id="88beb-149">-ProbeId</span></span>
<span data-ttu-id="88beb-150">Określa identyfikator współpracownika, który ma skojarzyć z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="88beb-151">— Protokół</span><span class="sxs-lookup"><span data-stu-id="88beb-151">-Protocol</span></span>
<span data-ttu-id="88beb-152">Określa protokół, który jest do siebie dopasujony przez regułę równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="88beb-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="88beb-153">Dopuszczalne wartości dla tego parametru to: Tcp lub Udp.</span><span class="sxs-lookup"><span data-stu-id="88beb-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="88beb-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88beb-154">-Confirm</span></span>
<span data-ttu-id="88beb-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88beb-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88beb-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88beb-156">-WhatIf</span></span>
<span data-ttu-id="88beb-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88beb-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88beb-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="88beb-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88beb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88beb-159">CommonParameters</span></span>
<span data-ttu-id="88beb-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88beb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88beb-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88beb-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88beb-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88beb-162">INPUTS</span></span>

### <span data-ttu-id="88beb-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="88beb-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="88beb-164">System.String</span><span class="sxs-lookup"><span data-stu-id="88beb-164">System.String</span></span>

### <span data-ttu-id="88beb-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="88beb-165">System.Int32</span></span>

### <span data-ttu-id="88beb-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="88beb-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="88beb-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="88beb-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="88beb-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="88beb-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="88beb-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88beb-169">OUTPUTS</span></span>

### <span data-ttu-id="88beb-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="88beb-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="88beb-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88beb-171">NOTES</span></span>

## <span data-ttu-id="88beb-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88beb-172">RELATED LINKS</span></span>

[<span data-ttu-id="88beb-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88beb-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="88beb-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88beb-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="88beb-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88beb-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="88beb-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88beb-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="88beb-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88beb-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)



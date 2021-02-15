---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193650"
---
# <span data-ttu-id="c2ffc-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2ffc-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c2ffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ffc-103">Tworzy konfigurację reguły dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c2ffc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2ffc-104">SYNTAX</span></span>

### <span data-ttu-id="c2ffc-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="c2ffc-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ffc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ffc-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ffc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2ffc-107">DESCRIPTION</span></span>
<span data-ttu-id="c2ffc-108">Polecenie **cmdlet New-AzLoadBalancerRuleConfig** tworzy konfigurację reguły dla narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c2ffc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2ffc-109">EXAMPLES</span></span>

### <span data-ttu-id="c2ffc-110">Przykład 1. Tworzenie konfiguracji reguły dla narzędzia Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="c2ffc-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="c2ffc-111">Pierwsze trzy polecenia set up a public IP, a front end, and a do the rule configuration in the forth command.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="c2ffc-112">Polecenie Forth tworzy nową regułę o nazwie MyLBrule z określonymi specyfikacjami.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="c2ffc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2ffc-113">PARAMETERS</span></span>

### <span data-ttu-id="c2ffc-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2ffc-114">-BackendAddressPool</span></span>
<span data-ttu-id="c2ffc-115">Określa obiekt **BackendAddressPool** do skojarzenia z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c2ffc-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c2ffc-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="c2ffc-117">Określa identyfikator obiektu **BackendAddressPool,** który ma być skojarzony z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c2ffc-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c2ffc-118">-BackendPort</span></span>
<span data-ttu-id="c2ffc-119">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c2ffc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ffc-120">-DefaultProfile</span></span>
<span data-ttu-id="c2ffc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2ffc-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c2ffc-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c2ffc-123">Konfiguruje usługę SNAT dla maszyn wirtualnych w puli zaplecza w celu użycia adresu publicznegoip określonego w frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="c2ffc-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c2ffc-124">-EnableFloatingIP</span></span>
<span data-ttu-id="c2ffc-125">Wskazuje, że to polecenie cmdlet umożliwia przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c2ffc-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c2ffc-126">-EnableTcpReset</span></span>
<span data-ttu-id="c2ffc-127">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c2ffc-128">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c2ffc-129">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ffc-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c2ffc-130">Określa listę frontoronowych adresów IP do skojarzenia z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c2ffc-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c2ffc-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c2ffc-132">Określa identyfikator konfiguracji frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c2ffc-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2ffc-133">-FrontendPort</span></span>
<span data-ttu-id="c2ffc-134">Określa port frontonie, który jest do siebie dopasowany przez konfigurację reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c2ffc-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c2ffc-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c2ffc-136">Określa czas (w minutach), przez który stan konwersacji jest utrzymywany w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c2ffc-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c2ffc-137">-LoadDistribution</span></span>
<span data-ttu-id="c2ffc-138">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-138">Specifies a load distribution.</span></span>
<span data-ttu-id="c2ffc-139">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2ffc-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2ffc-140">Domyślne</span><span class="sxs-lookup"><span data-stu-id="c2ffc-140">Default</span></span>
- <span data-ttu-id="c2ffc-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="c2ffc-141">SourceIP</span></span>
- <span data-ttu-id="c2ffc-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="c2ffc-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="c2ffc-143">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2ffc-143">-Name</span></span>
<span data-ttu-id="c2ffc-144">Określa nazwę reguły równoważenia obciążenia, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c2ffc-145">— Dor.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-145">-Probe</span></span>
<span data-ttu-id="c2ffc-146">Określa wartość do skojarzenia z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c2ffc-147">- NaiwnyId</span><span class="sxs-lookup"><span data-stu-id="c2ffc-147">-ProbeId</span></span>
<span data-ttu-id="c2ffc-148">Określa identyfikator współpracownika, który ma skojarzyć z konfiguracją reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c2ffc-149">— Protokół</span><span class="sxs-lookup"><span data-stu-id="c2ffc-149">-Protocol</span></span>
<span data-ttu-id="c2ffc-150">Określa protokół, do który jest do dopasowana konfiguracja reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="c2ffc-151">Dopuszczalne wartości dla tego parametru to: Tcp lub Udp.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c2ffc-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2ffc-152">-Confirm</span></span>
<span data-ttu-id="c2ffc-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ffc-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ffc-154">-WhatIf</span></span>
<span data-ttu-id="c2ffc-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2ffc-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ffc-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ffc-157">CommonParameters</span></span>
<span data-ttu-id="c2ffc-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ffc-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ffc-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ffc-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ffc-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2ffc-160">INPUTS</span></span>

### <span data-ttu-id="c2ffc-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c2ffc-161">System.String</span></span>

### <span data-ttu-id="c2ffc-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c2ffc-162">System.Int32</span></span>

### <span data-ttu-id="c2ffc-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2ffc-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="c2ffc-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2ffc-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="c2ffc-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="c2ffc-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="c2ffc-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2ffc-166">OUTPUTS</span></span>

### <span data-ttu-id="c2ffc-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="c2ffc-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="c2ffc-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2ffc-168">NOTES</span></span>

## <span data-ttu-id="c2ffc-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2ffc-169">RELATED LINKS</span></span>

[<span data-ttu-id="c2ffc-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2ffc-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c2ffc-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2ffc-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c2ffc-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2ffc-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c2ffc-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2ffc-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)



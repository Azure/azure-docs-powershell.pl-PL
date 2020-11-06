---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 871982993492ba8eb06d818759e31d3c3500c1d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545052"
---
# <span data-ttu-id="2fc04-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fc04-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="2fc04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fc04-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc04-103">Tworzy konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fc04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fc04-104">SYNTAX</span></span>

### <span data-ttu-id="2fc04-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2fc04-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc04-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc04-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc04-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2fc04-107">DESCRIPTION</span></span>
<span data-ttu-id="2fc04-108">Polecenie cmdlet **New-AzureRmLoadBalancerRuleConfig** tworzy konfigurację reguły dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc04-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="2fc04-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fc04-109">EXAMPLES</span></span>

### <span data-ttu-id="2fc04-110">1: Tworzenie konfiguracji reguły dla modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2fc04-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="2fc04-111">Pierwsze trzy polecenia konfigurują publiczny adres IP, fronton i sondę dla konfiguracji reguły w z poleceniu z dalej.</span><span class="sxs-lookup"><span data-stu-id="2fc04-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="2fc04-112">Polecenie Dalej powoduje utworzenie nowej reguły o nazwie MyLBrule z określonymi specyfikacjami.</span><span class="sxs-lookup"><span data-stu-id="2fc04-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="2fc04-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fc04-113">PARAMETERS</span></span>

### <span data-ttu-id="2fc04-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2fc04-114">-BackendAddressPool</span></span>
<span data-ttu-id="2fc04-115">Określa obiekt **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2fc04-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2fc04-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="2fc04-117">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2fc04-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="2fc04-118">-BackendPort</span></span>
<span data-ttu-id="2fc04-119">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2fc04-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc04-120">-DefaultProfile</span></span>
<span data-ttu-id="2fc04-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc04-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc04-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="2fc04-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="2fc04-123">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="2fc04-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="2fc04-124">-EnableFloatingIP</span></span>
<span data-ttu-id="2fc04-125">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="2fc04-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="2fc04-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2fc04-126">-EnableTcpReset</span></span>
<span data-ttu-id="2fc04-127">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="2fc04-128">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="2fc04-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="2fc04-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fc04-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2fc04-130">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2fc04-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2fc04-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="2fc04-132">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="2fc04-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="2fc04-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="2fc04-133">-FrontendPort</span></span>
<span data-ttu-id="2fc04-134">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2fc04-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2fc04-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2fc04-136">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="2fc04-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="2fc04-137">-LoadDistribution</span></span>
<span data-ttu-id="2fc04-138">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-138">Specifies a load distribution.</span></span>
<span data-ttu-id="2fc04-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2fc04-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2fc04-140">Domyślne</span><span class="sxs-lookup"><span data-stu-id="2fc04-140">Default</span></span>
- <span data-ttu-id="2fc04-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="2fc04-141">SourceIP</span></span>
- <span data-ttu-id="2fc04-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="2fc04-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="2fc04-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2fc04-143">-Name</span></span>
<span data-ttu-id="2fc04-144">Określa nazwę reguły równoważenia obciążenia tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fc04-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2fc04-145">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="2fc04-145">-Probe</span></span>
<span data-ttu-id="2fc04-146">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2fc04-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="2fc04-147">-ProbeId</span></span>
<span data-ttu-id="2fc04-148">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2fc04-149">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="2fc04-149">-Protocol</span></span>
<span data-ttu-id="2fc04-150">Określa protokół zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2fc04-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="2fc04-151">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="2fc04-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="2fc04-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fc04-152">-Confirm</span></span>
<span data-ttu-id="2fc04-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fc04-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc04-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc04-154">-WhatIf</span></span>
<span data-ttu-id="2fc04-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fc04-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fc04-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2fc04-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc04-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc04-157">CommonParameters</span></span>
<span data-ttu-id="2fc04-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc04-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc04-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc04-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc04-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fc04-160">INPUTS</span></span>

### <span data-ttu-id="2fc04-161">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2fc04-161">None</span></span>

## <span data-ttu-id="2fc04-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fc04-162">OUTPUTS</span></span>

### <span data-ttu-id="2fc04-163">Microsoft. Azure. Commands. Network. models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="2fc04-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="2fc04-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fc04-164">NOTES</span></span>

## <span data-ttu-id="2fc04-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fc04-165">RELATED LINKS</span></span>

[<span data-ttu-id="2fc04-166">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fc04-166">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2fc04-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fc04-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2fc04-168">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fc04-168">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2fc04-169">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fc04-169">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)



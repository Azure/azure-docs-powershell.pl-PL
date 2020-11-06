---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: a584d473354fd900b117f5661dc738b239f3a92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547444"
---
# <span data-ttu-id="7d2a2-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d2a2-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7d2a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2a2-103">Ustawia stan celu dla konfiguracji reguł modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d2a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d2a2-104">SYNTAX</span></span>

### <span data-ttu-id="7d2a2-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d2a2-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d2a2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d2a2-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2a2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7d2a2-107">DESCRIPTION</span></span>
<span data-ttu-id="7d2a2-108">Polecenie cmdlet **Set-AzureRmLoadBalancerRuleConfig** ustawia stan celu dla konfiguracji reguł modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="7d2a2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d2a2-109">EXAMPLES</span></span>

### <span data-ttu-id="7d2a2-110">Przykład 1: modyfikowanie konfiguracji reguły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7d2a2-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="7d2a2-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="7d2a2-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerRuleConfig, które umożliwia dodanie reguły o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="7d2a2-113">Trzecia komenda przekazuje modułowi równoważenia obciążenia **wartość Set-AzureRmLoadBalancerRuleConfig** , która ustawia konfigurację nowej reguły.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="7d2a2-114">Zauważ, że konfiguracja nie umożliwia przestawenia adresu IP, który został włączony przez poprzednie polecenie.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="7d2a2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d2a2-115">PARAMETERS</span></span>

### <span data-ttu-id="7d2a2-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d2a2-116">-BackendAddressPool</span></span>
<span data-ttu-id="7d2a2-117">Określa obiekt **BackendAddressPool** , który ma zostać skojarzony z regułą modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="7d2a2-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7d2a2-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="7d2a2-119">Określa identyfikator obiektu **BackendAddressPool** , który ma zostać skojarzony z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7d2a2-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7d2a2-120">-BackendPort</span></span>
<span data-ttu-id="7d2a2-121">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="7d2a2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2a2-122">-DefaultProfile</span></span>
<span data-ttu-id="7d2a2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d2a2-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="7d2a2-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="7d2a2-125">Konfiguruje w puli zaplecza na potrzeby wirtualnych adresów sieciowych w celu użycia adresu publicIP określonego na frontonie reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="7d2a2-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7d2a2-126">-EnableFloatingIP</span></span>
<span data-ttu-id="7d2a2-127">Wskazuje, że to polecenie cmdlet włącza przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="7d2a2-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7d2a2-128">-EnableTcpReset</span></span>
<span data-ttu-id="7d2a2-129">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="7d2a2-130">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7d2a2-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d2a2-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="7d2a2-132">Określa listę zewnętrznych adresów IP, które należy skojarzyć z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7d2a2-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7d2a2-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="7d2a2-134">Określa identyfikator konfiguracji adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="7d2a2-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7d2a2-135">-FrontendPort</span></span>
<span data-ttu-id="7d2a2-136">Określa port frontonu zgodny z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7d2a2-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7d2a2-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7d2a2-138">Określa czas (w minutach) przechowywania stanu konwersacji w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="7d2a2-139">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7d2a2-139">-LoadBalancer</span></span>
<span data-ttu-id="7d2a2-140">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-140">Specifies a load balancer.</span></span>
<span data-ttu-id="7d2a2-141">To polecenie cmdlet ustawia konfigurację reguły stanu celu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-141">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d2a2-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="7d2a2-142">-LoadDistribution</span></span>
<span data-ttu-id="7d2a2-143">Określa rozkład obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-143">Specifies a load distribution.</span></span>
<span data-ttu-id="7d2a2-144">Dopuszczalne wartości tego parametru to: SourceIP oraz SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="7d2a2-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d2a2-145">-Name</span></span>
<span data-ttu-id="7d2a2-146">Określa nazwę modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="7d2a2-147">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="7d2a2-147">-Probe</span></span>
<span data-ttu-id="7d2a2-148">Określa sondę do skojarzenia z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7d2a2-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="7d2a2-149">-ProbeId</span></span>
<span data-ttu-id="7d2a2-150">Określa identyfikator sondy, która ma być skojarzona z konfiguracją reguły modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="7d2a2-151">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="7d2a2-151">-Protocol</span></span>
<span data-ttu-id="7d2a2-152">Określa protokół zgodny z regułą modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="7d2a2-153">Dopuszczalne wartości tego parametru to: TCP lub UDP.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="7d2a2-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d2a2-154">-Confirm</span></span>
<span data-ttu-id="7d2a2-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d2a2-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2a2-156">-WhatIf</span></span>
<span data-ttu-id="7d2a2-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d2a2-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d2a2-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2a2-159">CommonParameters</span></span>
<span data-ttu-id="7d2a2-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2a2-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2a2-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2a2-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2a2-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d2a2-162">INPUTS</span></span>

### <span data-ttu-id="7d2a2-163">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d2a2-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="7d2a2-164">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d2a2-164">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="7d2a2-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d2a2-165">OUTPUTS</span></span>

### <span data-ttu-id="7d2a2-166">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d2a2-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7d2a2-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d2a2-167">NOTES</span></span>

## <span data-ttu-id="7d2a2-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d2a2-168">RELATED LINKS</span></span>

[<span data-ttu-id="7d2a2-169">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d2a2-169">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7d2a2-170">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d2a2-170">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7d2a2-171">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d2a2-171">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7d2a2-172">Nowe — AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d2a2-172">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="7d2a2-173">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d2a2-173">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 44f8304ce1ee79c114dc4054c8dd7fff3dcd22fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006506"
---
# <span data-ttu-id="bab8a-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bab8a-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="bab8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bab8a-102">SYNOPSIS</span></span>
<span data-ttu-id="bab8a-103">Dodaje konfigurację reguły nat ruchu przychodzącego do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bab8a-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="bab8a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bab8a-104">SYNTAX</span></span>

### <span data-ttu-id="bab8a-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="bab8a-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bab8a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bab8a-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bab8a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bab8a-107">DESCRIPTION</span></span>
<span data-ttu-id="bab8a-108">Polecenie **cmdlet Add-AzLoadBalancerInboundNatRuleConfig** dodaje konfigurację reguły translacji przychodzącego adresu sieciowego (NAT) do narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bab8a-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="bab8a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bab8a-109">EXAMPLES</span></span>

### <span data-ttu-id="bab8a-110">Przykład 1. Dodawanie konfiguracji reguły nat ruchu przychodzącego do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="bab8a-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="bab8a-111">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyloadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="bab8a-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="bab8a-112">Drugie polecenie korzysta z operatora potoku w celu przekazania równoważenia obciążenia w programie $slb do dodatku **Add-AzLoadBalancerInboundNatRuleConfig,** co powoduje dodanie konfiguracji reguły przychodzącego serwera NAT do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bab8a-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>
<span data-ttu-id="bab8a-113">Ostatnie polecenie ustawia konfigurację na równoważenie obciążenia, jeśli nie wykonasz ustawienia Set-AzLoadBalancer, zmiany nie zostaną zastosowane do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bab8a-113">The last command sets the configuration to the loadbalancer, if you don't perform Set-AzLoadBalancer, your changes will not be applied to the loadbalancer.</span></span>

## <span data-ttu-id="bab8a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bab8a-114">PARAMETERS</span></span>

### <span data-ttu-id="bab8a-115">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="bab8a-115">-BackendPort</span></span>
<span data-ttu-id="bab8a-116">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="bab8a-116">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="bab8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab8a-117">-DefaultProfile</span></span>
<span data-ttu-id="bab8a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bab8a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bab8a-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="bab8a-119">-EnableFloatingIP</span></span>
<span data-ttu-id="bab8a-120">Wskazuje, że to polecenie cmdlet umożliwia przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="bab8a-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="bab8a-121">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="bab8a-121">-EnableTcpReset</span></span>
<span data-ttu-id="bab8a-122">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="bab8a-122">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="bab8a-123">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="bab8a-123">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="bab8a-124">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bab8a-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="bab8a-125">Określa listę frontoronowych adresów IP do skojarzenia z konfiguracją reguły nat ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="bab8a-125">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="bab8a-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bab8a-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="bab8a-127">Określa identyfikator dla konfiguracji frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="bab8a-127">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="bab8a-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bab8a-128">-FrontendPort</span></span>
<span data-ttu-id="bab8a-129">Określa port frontoronu, do których jest dopasowana konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="bab8a-129">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="bab8a-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bab8a-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bab8a-131">Określa czas (w minutach), przez który stan konwersacji jest utrzymywany w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bab8a-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="bab8a-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bab8a-132">-LoadBalancer</span></span>
<span data-ttu-id="bab8a-133">Określa obiekt **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="bab8a-133">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="bab8a-134">To polecenie cmdlet dodaje konfigurację reguły nat ruchu przychodzącego do równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bab8a-134">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="bab8a-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bab8a-135">-Name</span></span>
<span data-ttu-id="bab8a-136">Określa nazwę konfiguracji przychodzącej reguły NAT do dodania.</span><span class="sxs-lookup"><span data-stu-id="bab8a-136">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="bab8a-137">— Protokół</span><span class="sxs-lookup"><span data-stu-id="bab8a-137">-Protocol</span></span>
<span data-ttu-id="bab8a-138">Określa protokół, do których jest dopasowana reguła nat ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="bab8a-138">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="bab8a-139">Dopuszczalne wartości dla tego parametru to: Tcp lub Udp.</span><span class="sxs-lookup"><span data-stu-id="bab8a-139">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="bab8a-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bab8a-140">-Confirm</span></span>
<span data-ttu-id="bab8a-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bab8a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bab8a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bab8a-142">-WhatIf</span></span>
<span data-ttu-id="bab8a-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bab8a-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bab8a-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bab8a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bab8a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab8a-145">CommonParameters</span></span>
<span data-ttu-id="bab8a-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bab8a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab8a-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab8a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab8a-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bab8a-148">INPUTS</span></span>

### <span data-ttu-id="bab8a-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bab8a-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="bab8a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="bab8a-150">System.String</span></span>

### <span data-ttu-id="bab8a-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bab8a-151">System.Int32</span></span>

### <span data-ttu-id="bab8a-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bab8a-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="bab8a-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bab8a-153">OUTPUTS</span></span>

### <span data-ttu-id="bab8a-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bab8a-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bab8a-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bab8a-155">NOTES</span></span>

## <span data-ttu-id="bab8a-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bab8a-156">RELATED LINKS</span></span>

[<span data-ttu-id="bab8a-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bab8a-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="bab8a-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bab8a-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bab8a-159">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bab8a-159">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bab8a-160">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bab8a-160">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bab8a-161">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bab8a-161">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="bab8a-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bab8a-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)



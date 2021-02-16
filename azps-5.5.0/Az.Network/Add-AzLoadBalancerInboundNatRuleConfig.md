---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193962"
---
# <span data-ttu-id="be2ae-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="be2ae-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="be2ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="be2ae-103">Dodaje konfigurację reguły nat ruchu przychodzącego do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="be2ae-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="be2ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be2ae-104">SYNTAX</span></span>

### <span data-ttu-id="be2ae-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="be2ae-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2ae-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="be2ae-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be2ae-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="be2ae-107">DESCRIPTION</span></span>
<span data-ttu-id="be2ae-108">Polecenie **cmdlet Add-AzLoadBalancerInboundNatRuleConfig** dodaje konfigurację reguły translacji przychodzącego adresu sieciowego (NAT) do narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be2ae-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="be2ae-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be2ae-109">EXAMPLES</span></span>

### <span data-ttu-id="be2ae-110">Przykład 1. Dodawanie konfiguracji reguły nat ruchu przychodzącego do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="be2ae-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="be2ae-111">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyloadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="be2ae-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="be2ae-112">Drugie polecenie korzysta z operatora potoku w celu przekazania równoważenia obciążenia w programie $slb do dodatku **Add-AzLoadBalancerInboundNatRuleConfig,** co powoduje dodanie konfiguracji reguły nat ruchu przychodzącego do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="be2ae-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="be2ae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be2ae-113">PARAMETERS</span></span>

### <span data-ttu-id="be2ae-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="be2ae-114">-BackendPort</span></span>
<span data-ttu-id="be2ae-115">Określa port zaplecza dla ruchu zgodnego z konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="be2ae-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="be2ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2ae-116">-DefaultProfile</span></span>
<span data-ttu-id="be2ae-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be2ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be2ae-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="be2ae-118">-EnableFloatingIP</span></span>
<span data-ttu-id="be2ae-119">Wskazuje, że to polecenie cmdlet umożliwia przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="be2ae-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="be2ae-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="be2ae-120">-EnableTcpReset</span></span>
<span data-ttu-id="be2ae-121">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="be2ae-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="be2ae-122">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="be2ae-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="be2ae-123">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="be2ae-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="be2ae-124">Określa listę frontoronowych adresów IP do skojarzenia z konfiguracją reguły nat ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="be2ae-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="be2ae-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="be2ae-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="be2ae-126">Określa identyfikator dla konfiguracji frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="be2ae-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="be2ae-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="be2ae-127">-FrontendPort</span></span>
<span data-ttu-id="be2ae-128">Określa port frontoronu, do których jest dopasowana konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="be2ae-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="be2ae-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="be2ae-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="be2ae-130">Określa czas (w minutach), przez który stan konwersacji jest utrzymywany w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="be2ae-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="be2ae-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be2ae-131">-LoadBalancer</span></span>
<span data-ttu-id="be2ae-132">Określa obiekt **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="be2ae-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="be2ae-133">To polecenie cmdlet dodaje konfigurację reguły nat ruchu przychodzącego do równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="be2ae-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="be2ae-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="be2ae-134">-Name</span></span>
<span data-ttu-id="be2ae-135">Określa nazwę konfiguracji reguły nat ruchu przychodzącego do dodania.</span><span class="sxs-lookup"><span data-stu-id="be2ae-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="be2ae-136">— Protokół</span><span class="sxs-lookup"><span data-stu-id="be2ae-136">-Protocol</span></span>
<span data-ttu-id="be2ae-137">Określa protokół, do których jest dopasowana reguła nat ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="be2ae-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="be2ae-138">Dopuszczalne wartości dla tego parametru to: Tcp lub Udp.</span><span class="sxs-lookup"><span data-stu-id="be2ae-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="be2ae-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be2ae-139">-Confirm</span></span>
<span data-ttu-id="be2ae-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be2ae-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be2ae-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be2ae-141">-WhatIf</span></span>
<span data-ttu-id="be2ae-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be2ae-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be2ae-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="be2ae-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be2ae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2ae-144">CommonParameters</span></span>
<span data-ttu-id="be2ae-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be2ae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2ae-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be2ae-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2ae-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be2ae-147">INPUTS</span></span>

### <span data-ttu-id="be2ae-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be2ae-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="be2ae-149">System.String</span><span class="sxs-lookup"><span data-stu-id="be2ae-149">System.String</span></span>

### <span data-ttu-id="be2ae-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="be2ae-150">System.Int32</span></span>

### <span data-ttu-id="be2ae-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="be2ae-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="be2ae-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be2ae-152">OUTPUTS</span></span>

### <span data-ttu-id="be2ae-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be2ae-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="be2ae-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be2ae-154">NOTES</span></span>

## <span data-ttu-id="be2ae-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be2ae-155">RELATED LINKS</span></span>

[<span data-ttu-id="be2ae-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be2ae-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="be2ae-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="be2ae-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="be2ae-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="be2ae-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="be2ae-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="be2ae-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="be2ae-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be2ae-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="be2ae-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="be2ae-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)



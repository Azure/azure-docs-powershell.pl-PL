---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184194"
---
# <span data-ttu-id="dc835-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc835-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="dc835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc835-102">SYNOPSIS</span></span>
<span data-ttu-id="dc835-103">Ustawia konfigurację reguły nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="dc835-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="dc835-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc835-104">SYNTAX</span></span>

### <span data-ttu-id="dc835-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="dc835-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc835-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc835-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc835-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc835-107">DESCRIPTION</span></span>
<span data-ttu-id="dc835-108">Polecenie cmdlet **Set-AzLoadBalancerInboundNatRuleConfig** ustawia konfigurację reguły translacji przychodzącego adresu sieciowego (NAT) dla narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dc835-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="dc835-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc835-109">EXAMPLES</span></span>

### <span data-ttu-id="dc835-110">Przykład 1. Modyfikowanie konfiguracji reguły nat ruchu przychodzącego w równoważeniu obciążenia</span><span class="sxs-lookup"><span data-stu-id="dc835-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="dc835-111">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w $slb zmienną.</span><span class="sxs-lookup"><span data-stu-id="dc835-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="dc835-112">Drugie polecenie korzysta z operatora potoku w celu przekazania równoważenia obciążenia w programie $slb do dodatku Add-AzLoadBalancerInboundNatRuleConfig, co powoduje dodanie do niego konfiguracji reguły przychodzącego serwera NAT.</span><span class="sxs-lookup"><span data-stu-id="dc835-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="dc835-113">Trzecie polecenie przekazuje równoważenie obciążenia do polecenia **Set-AzLoadBalancerInboundNatRuleConfig,** które zapisuje i aktualizuje konfigurację reguł nat ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="dc835-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="dc835-114">Pamiętaj, że konfiguracja reguły została ustawiona bez włączania przestawnego adresu IP, który został włączony przez poprzednie polecenie.</span><span class="sxs-lookup"><span data-stu-id="dc835-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="dc835-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc835-115">PARAMETERS</span></span>

### <span data-ttu-id="dc835-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="dc835-116">-BackendPort</span></span>
<span data-ttu-id="dc835-117">Określa port zaplecza dla ruchu zgodnego z tą konfiguracją reguły.</span><span class="sxs-lookup"><span data-stu-id="dc835-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="dc835-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc835-118">-DefaultProfile</span></span>
<span data-ttu-id="dc835-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc835-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc835-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="dc835-120">-EnableFloatingIP</span></span>
<span data-ttu-id="dc835-121">Wskazuje, że to polecenie cmdlet umożliwia przestawny adres IP dla konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="dc835-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="dc835-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="dc835-122">-EnableTcpReset</span></span>
<span data-ttu-id="dc835-123">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="dc835-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="dc835-124">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="dc835-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="dc835-125">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc835-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="dc835-126">Określa listę frontoronowych adresów IP do skojarzenia z konfiguracją reguły nat ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="dc835-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="dc835-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dc835-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="dc835-128">Określa identyfikator konfiguracji frontoronu adresu IP.</span><span class="sxs-lookup"><span data-stu-id="dc835-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="dc835-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="dc835-129">-FrontendPort</span></span>
<span data-ttu-id="dc835-130">Określa port frontonie, który jest do siebie dopasowany przez konfigurację reguły równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="dc835-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="dc835-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="dc835-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="dc835-132">Określa czas (w minutach), przez który stan konwersacji jest utrzymywany w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="dc835-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="dc835-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dc835-133">-LoadBalancer</span></span>
<span data-ttu-id="dc835-134">Określa równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="dc835-134">Specifies a load balancer.</span></span>
<span data-ttu-id="dc835-135">To polecenie cmdlet ustawia konfigurację reguły nat ruchu przychodzącego dla równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="dc835-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc835-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dc835-136">-Name</span></span>
<span data-ttu-id="dc835-137">Określa nazwę konfiguracji reguły nat ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="dc835-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="dc835-138">— Protokół</span><span class="sxs-lookup"><span data-stu-id="dc835-138">-Protocol</span></span>
<span data-ttu-id="dc835-139">Określa protokół, do który jest do dopasowana konfiguracja reguły nat ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="dc835-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="dc835-140">Dopuszczalne wartości dla tego parametru to: Tcp lub Udp.</span><span class="sxs-lookup"><span data-stu-id="dc835-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="dc835-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc835-141">-Confirm</span></span>
<span data-ttu-id="dc835-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dc835-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc835-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc835-143">-WhatIf</span></span>
<span data-ttu-id="dc835-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc835-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc835-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dc835-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc835-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc835-146">CommonParameters</span></span>
<span data-ttu-id="dc835-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc835-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc835-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc835-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc835-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc835-149">INPUTS</span></span>

### <span data-ttu-id="dc835-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dc835-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="dc835-151">System.String</span><span class="sxs-lookup"><span data-stu-id="dc835-151">System.String</span></span>

### <span data-ttu-id="dc835-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="dc835-152">System.Int32</span></span>

### <span data-ttu-id="dc835-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc835-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="dc835-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc835-154">OUTPUTS</span></span>

### <span data-ttu-id="dc835-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dc835-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dc835-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc835-156">NOTES</span></span>

## <span data-ttu-id="dc835-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc835-157">RELATED LINKS</span></span>

[<span data-ttu-id="dc835-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc835-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dc835-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dc835-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="dc835-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc835-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dc835-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc835-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dc835-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc835-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)



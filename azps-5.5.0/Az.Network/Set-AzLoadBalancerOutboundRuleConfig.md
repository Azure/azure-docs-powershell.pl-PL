---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179330"
---
# <span data-ttu-id="76060-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76060-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="76060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76060-102">SYNOPSIS</span></span>
<span data-ttu-id="76060-103">Ustawia konfigurację reguły ruchu wychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="76060-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="76060-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76060-104">SYNTAX</span></span>

### <span data-ttu-id="76060-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="76060-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76060-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="76060-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76060-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="76060-107">DESCRIPTION</span></span>
<span data-ttu-id="76060-108">Polecenie **cmdlet Set-AzLoadBalancerOutboundRuleConfig** ustawia konfigurację reguły ruchu wychodzącego dla narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="76060-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="76060-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76060-109">EXAMPLES</span></span>

### <span data-ttu-id="76060-110">Przykład 1. Modyfikowanie konfiguracji reguły ruchu wychodzącego w równoważeniu obciążenia</span><span class="sxs-lookup"><span data-stu-id="76060-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="76060-111">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w $slb zmienną.</span><span class="sxs-lookup"><span data-stu-id="76060-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="76060-112">Drugie polecenie korzysta z operatora potoku w celu przekazania równoważenia obciążenia w programie $slb do dodatku Add-AzLoadBalancerOutboundRuleConfig, co powoduje dodanie do niego konfiguracji reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="76060-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="76060-113">Trzecie polecenie przekazuje równoważenie obciążenia do polecenia **Set-AzLoadBalancerOutboundRuleConfig,** które zapisuje i aktualizuje konfigurację reguł ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="76060-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="76060-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76060-114">PARAMETERS</span></span>

### <span data-ttu-id="76060-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="76060-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="76060-116">Liczba portów wychodzących, które mają być używane na pasku nat.</span><span class="sxs-lookup"><span data-stu-id="76060-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="76060-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76060-117">-BackendAddressPool</span></span>
<span data-ttu-id="76060-118">Odwołanie do puli dipów.</span><span class="sxs-lookup"><span data-stu-id="76060-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="76060-119">Ruch wychodzący jest losowo ładowany na wielu serwerach IP w ramach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="76060-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="76060-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="76060-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="76060-121">Odwołanie do puli dipów.</span><span class="sxs-lookup"><span data-stu-id="76060-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="76060-122">Ruch wychodzący jest losowo ładowany na wielu serwerach IP w ramach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="76060-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="76060-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76060-123">-DefaultProfile</span></span>
<span data-ttu-id="76060-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76060-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76060-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="76060-125">-EnableTcpReset</span></span>
<span data-ttu-id="76060-126">Odbieranie dwukierunkowego resetowania protokołu TCP w przypadku bezczynnego limitu czasu przepływu TCP lub nieoczekiwanego zakończenia połączenia.</span><span class="sxs-lookup"><span data-stu-id="76060-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="76060-127">Ten element jest używany tylko wtedy, gdy protokół ma ustawioną wartość TCP.</span><span class="sxs-lookup"><span data-stu-id="76060-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="76060-128">- FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="76060-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="76060-129">Adresy IP frontendu do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="76060-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="76060-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="76060-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="76060-131">Limit czasu dla bezczynne połączenie TCP</span><span class="sxs-lookup"><span data-stu-id="76060-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="76060-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="76060-132">-LoadBalancer</span></span>
<span data-ttu-id="76060-133">Odwołanie do zasobu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="76060-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="76060-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="76060-134">-Name</span></span>
<span data-ttu-id="76060-135">Nazwa reguły wychodzącej.</span><span class="sxs-lookup"><span data-stu-id="76060-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="76060-136">— Protokół</span><span class="sxs-lookup"><span data-stu-id="76060-136">-Protocol</span></span>
<span data-ttu-id="76060-137">Protokół — TCP, UDP lub All</span><span class="sxs-lookup"><span data-stu-id="76060-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="76060-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76060-138">-Confirm</span></span>
<span data-ttu-id="76060-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76060-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76060-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76060-140">-WhatIf</span></span>
<span data-ttu-id="76060-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76060-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76060-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="76060-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76060-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76060-143">CommonParameters</span></span>
<span data-ttu-id="76060-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76060-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76060-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76060-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76060-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76060-146">INPUTS</span></span>

### <span data-ttu-id="76060-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="76060-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="76060-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="76060-148">System.Int32</span></span>

### <span data-ttu-id="76060-149">System.String</span><span class="sxs-lookup"><span data-stu-id="76060-149">System.String</span></span>

### <span data-ttu-id="76060-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="76060-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="76060-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76060-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="76060-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76060-152">OUTPUTS</span></span>

### <span data-ttu-id="76060-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="76060-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="76060-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76060-154">NOTES</span></span>

## <span data-ttu-id="76060-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76060-155">RELATED LINKS</span></span>

[<span data-ttu-id="76060-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76060-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="76060-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76060-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="76060-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76060-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="76060-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76060-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

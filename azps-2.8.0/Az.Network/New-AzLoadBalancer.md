---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 4e642f3aa93baad03a5b79a1736027353d5194bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869924"
---
# <span data-ttu-id="49b39-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49b39-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="49b39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49b39-102">SYNOPSIS</span></span>
<span data-ttu-id="49b39-103">Umożliwia utworzenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-103">Creates a load balancer.</span></span>

## <span data-ttu-id="49b39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49b39-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b39-105">Opis</span><span class="sxs-lookup"><span data-stu-id="49b39-105">DESCRIPTION</span></span>
<span data-ttu-id="49b39-106">Polecenie cmdlet **New-AzLoadBalancer** umożliwia utworzenie modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="49b39-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="49b39-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49b39-107">EXAMPLES</span></span>

### <span data-ttu-id="49b39-108">Przykład 1. Tworzenie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="49b39-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="49b39-109">Wdrożenie modułu równoważenia obciążenia wymaga wcześniejszego utworzenia kilku obiektów, a pierwsze siedem poleceń przedstawia sposób tworzenia tych obiektów.</span><span class="sxs-lookup"><span data-stu-id="49b39-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="49b39-110">Osiem poleceń powoduje utworzenie modułu równoważenia obciążenia o nazwie MyLoadBalancer w grupie zasób o nazwie moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="49b39-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="49b39-111">Dziewiąte i ostatnie polecenie otrzymuje nowe moduły równoważenia obciążenia w celu upewnienia się, że zostało pomyślnie utworzone.</span><span class="sxs-lookup"><span data-stu-id="49b39-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="49b39-112">Należy zauważyć, że w tym przykładzie przedstawiono tylko sposób tworzenia modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="49b39-113">Musisz też skonfigurować go za pomocą polecenia cmdlet Add-AzNetworkInterfaceIpConfig, aby przypisać karty sieciowe do różnych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="49b39-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="49b39-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49b39-114">PARAMETERS</span></span>

### <span data-ttu-id="49b39-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49b39-115">-AsJob</span></span>
<span data-ttu-id="49b39-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="49b39-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49b39-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="49b39-117">-BackendAddressPool</span></span>
<span data-ttu-id="49b39-118">Określa pulę adresów zaplecza, którą należy skojarzyć z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b39-119">-DefaultProfile</span></span>
<span data-ttu-id="49b39-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49b39-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49b39-121">-Force</span><span class="sxs-lookup"><span data-stu-id="49b39-121">-Force</span></span>
<span data-ttu-id="49b39-122">Wskazuje, że to polecenie cmdlet powoduje utworzenie modułu równoważenia obciążenia nawet wtedy, gdy istnieje już moduł równoważenia obciążenia o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="49b39-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="49b39-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="49b39-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="49b39-124">Określa listę zewnętrznych adresów IP, które należy skojarzyć z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="49b39-125">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="49b39-126">-InboundNatRule</span></span>
<span data-ttu-id="49b39-127">Określa listę reguł translacji adresów sieciowych (NAT), które mają zostać skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="49b39-128">-LoadBalancingRule</span></span>
<span data-ttu-id="49b39-129">Określa listę reguł równoważenia obciążenia, które mają zostać skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="49b39-130">-Location</span></span>
<span data-ttu-id="49b39-131">Określa region, w którym ma zostać utworzony moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="49b39-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49b39-132">-Name</span></span>
<span data-ttu-id="49b39-133">Określa nazwę tworzonego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="49b39-134">-OutboundRule</span></span>
<span data-ttu-id="49b39-135">Reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="49b39-135">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-136">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="49b39-136">-Probe</span></span>
<span data-ttu-id="49b39-137">Określa listę sondowań, które mają być skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b39-138">-ResourceGroupName</span></span>
<span data-ttu-id="49b39-139">Określa nazwę grupy zasobów, w której ma zostać utworzony moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="49b39-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="49b39-140">-Sku</span></span>
<span data-ttu-id="49b39-141">Nazwa SKU modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="49b39-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="49b39-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="49b39-142">-Tag</span></span>
<span data-ttu-id="49b39-143">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="49b39-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="49b39-144">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="49b39-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49b39-145">-Confirm</span></span>
<span data-ttu-id="49b39-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b39-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b39-147">-WhatIf</span></span>
<span data-ttu-id="49b39-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b39-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49b39-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49b39-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b39-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b39-150">CommonParameters</span></span>
<span data-ttu-id="49b39-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b39-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b39-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b39-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b39-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49b39-153">INPUTS</span></span>

### <span data-ttu-id="49b39-154">System. String</span><span class="sxs-lookup"><span data-stu-id="49b39-154">System.String</span></span>

### <span data-ttu-id="49b39-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="49b39-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="49b39-156">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="49b39-156">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="49b39-157">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="49b39-157">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="49b39-158">Microsoft. Azure. Commands. Network. models. PSLoadBalancingRule []</span><span class="sxs-lookup"><span data-stu-id="49b39-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="49b39-159">Microsoft. Azure. Commands. Network. models. PSProbe []</span><span class="sxs-lookup"><span data-stu-id="49b39-159">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="49b39-160">Microsoft. Azure. Commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="49b39-160">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="49b39-161">Microsoft. Azure. Commands. Network. models. PSInboundNatPool []</span><span class="sxs-lookup"><span data-stu-id="49b39-161">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="49b39-162">Microsoft. Azure. Commands. Network. models. PSOutboundRule []</span><span class="sxs-lookup"><span data-stu-id="49b39-162">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="49b39-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49b39-163">OUTPUTS</span></span>

### <span data-ttu-id="49b39-164">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49b39-164">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="49b39-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49b39-165">NOTES</span></span>

## <span data-ttu-id="49b39-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49b39-166">RELATED LINKS</span></span>

[<span data-ttu-id="49b39-167">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="49b39-167">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="49b39-168">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49b39-168">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="49b39-169">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49b39-169">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="49b39-170">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49b39-170">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

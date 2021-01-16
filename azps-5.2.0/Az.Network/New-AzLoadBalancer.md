---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354325"
---
# <span data-ttu-id="4ee72-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ee72-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="4ee72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ee72-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee72-103">Umożliwia utworzenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-103">Creates a load balancer.</span></span>

## <span data-ttu-id="4ee72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ee72-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee72-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ee72-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee72-106">Polecenie cmdlet **New-AzLoadBalancer** umożliwia utworzenie modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee72-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="4ee72-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ee72-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee72-108">Przykład 1. Tworzenie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4ee72-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4ee72-109">Wdrożenie modułu równoważenia obciążenia wymaga wcześniejszego utworzenia kilku obiektów, a pierwsze siedem poleceń przedstawia sposób tworzenia tych obiektów.</span><span class="sxs-lookup"><span data-stu-id="4ee72-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="4ee72-110">Osiem poleceń powoduje utworzenie modułu równoważenia obciążenia o nazwie MyLoadBalancer w grupie zasób o nazwie moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ee72-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="4ee72-111">Dziewiąte i ostatnie polecenie otrzymuje nowe moduły równoważenia obciążenia w celu upewnienia się, że zostało pomyślnie utworzone.</span><span class="sxs-lookup"><span data-stu-id="4ee72-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="4ee72-112">Należy zauważyć, że w tym przykładzie przedstawiono tylko sposób tworzenia modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="4ee72-113">Musisz też skonfigurować go za pomocą polecenia cmdlet Add-AzNetworkInterfaceIpConfig, aby przypisać karty sieciowe do różnych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="4ee72-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="4ee72-114">Przykład 2: Tworzenie globalnego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4ee72-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4ee72-115">Wdrożenie globalnego modułu równoważenia obciążenia wymaga wcześniejszego utworzenia kilku obiektów, a pięć pierwszych poleceń przedstawia sposób tworzenia tych obiektów.</span><span class="sxs-lookup"><span data-stu-id="4ee72-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="4ee72-116">Szóste polecenie tworzy moduł równoważenia obciążenia o nazwie MyLoadBalancer w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ee72-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="4ee72-117">Polecenie siódme i ostatnie powoduje utworzenie nowego modułu równoważenia obciążenia w celu upewnienia się, że został pomyślnie utworzony.</span><span class="sxs-lookup"><span data-stu-id="4ee72-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="4ee72-118">Należy zauważyć, że w tym przykładzie przedstawiono tylko sposób tworzenia globalnego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="4ee72-119">Musisz również skonfigurować tę usługę za pomocą polecenia cmdlet New-AzLoadBalancerBackendAddressConfig, aby przypisać identyfikatory ipconfig frontonu programu modułów równoważenia obciążenia do puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4ee72-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="4ee72-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ee72-120">PARAMETERS</span></span>

### <span data-ttu-id="4ee72-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ee72-121">-AsJob</span></span>
<span data-ttu-id="4ee72-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4ee72-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ee72-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ee72-123">-BackendAddressPool</span></span>
<span data-ttu-id="4ee72-124">Określa pulę adresów zaplecza, którą należy skojarzyć z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-124">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4ee72-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee72-125">-DefaultProfile</span></span>
<span data-ttu-id="4ee72-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee72-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee72-127">-Force</span><span class="sxs-lookup"><span data-stu-id="4ee72-127">-Force</span></span>
<span data-ttu-id="4ee72-128">Wskazuje, że to polecenie cmdlet powoduje utworzenie modułu równoważenia obciążenia nawet wtedy, gdy istnieje już moduł równoważenia obciążenia o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="4ee72-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="4ee72-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ee72-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4ee72-130">Określa listę zewnętrznych adresów IP, które należy skojarzyć z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4ee72-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="4ee72-131">-InboundNatPool</span></span>
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

### <span data-ttu-id="4ee72-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="4ee72-132">-InboundNatRule</span></span>
<span data-ttu-id="4ee72-133">Określa listę reguł translacji adresów sieciowych (NAT), które mają zostać skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4ee72-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="4ee72-134">-LoadBalancingRule</span></span>
<span data-ttu-id="4ee72-135">Określa listę reguł równoważenia obciążenia, które mają zostać skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4ee72-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4ee72-136">-Location</span></span>
<span data-ttu-id="4ee72-137">Określa region, w którym ma zostać utworzony moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="4ee72-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ee72-138">-Name</span></span>
<span data-ttu-id="4ee72-139">Określa nazwę tworzonego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="4ee72-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="4ee72-140">-OutboundRule</span></span>
<span data-ttu-id="4ee72-141">Reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="4ee72-141">The outbound rules.</span></span>

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

### <span data-ttu-id="4ee72-142">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="4ee72-142">-Probe</span></span>
<span data-ttu-id="4ee72-143">Określa listę sondowań, które mają być skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-143">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4ee72-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee72-144">-ResourceGroupName</span></span>
<span data-ttu-id="4ee72-145">Określa nazwę grupy zasobów, w której ma zostać utworzony moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="4ee72-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="4ee72-146">-Sku</span></span>
<span data-ttu-id="4ee72-147">Nazwa SKU modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="4ee72-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ee72-148">-Tag</span></span>
<span data-ttu-id="4ee72-149">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4ee72-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4ee72-150">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4ee72-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4ee72-151">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="4ee72-151">-Tier</span></span>
<span data-ttu-id="4ee72-152">Warstwa SKU modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4ee72-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="4ee72-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ee72-153">-Confirm</span></span>
<span data-ttu-id="4ee72-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee72-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee72-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee72-155">-WhatIf</span></span>
<span data-ttu-id="4ee72-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee72-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee72-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ee72-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee72-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee72-158">CommonParameters</span></span>
<span data-ttu-id="4ee72-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee72-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee72-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ee72-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee72-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ee72-161">INPUTS</span></span>

### <span data-ttu-id="4ee72-162">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee72-162">System.String</span></span>

### <span data-ttu-id="4ee72-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ee72-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4ee72-164">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="4ee72-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="4ee72-165">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="4ee72-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="4ee72-166">Microsoft. Azure. Commands. Network. models. PSLoadBalancingRule []</span><span class="sxs-lookup"><span data-stu-id="4ee72-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="4ee72-167">Microsoft. Azure. Commands. Network. models. PSProbe []</span><span class="sxs-lookup"><span data-stu-id="4ee72-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="4ee72-168">Microsoft. Azure. Commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="4ee72-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="4ee72-169">Microsoft. Azure. Commands. Network. models. PSInboundNatPool []</span><span class="sxs-lookup"><span data-stu-id="4ee72-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="4ee72-170">Microsoft. Azure. Commands. Network. models. PSOutboundRule []</span><span class="sxs-lookup"><span data-stu-id="4ee72-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="4ee72-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ee72-171">OUTPUTS</span></span>

### <span data-ttu-id="4ee72-172">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ee72-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4ee72-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ee72-173">NOTES</span></span>

## <span data-ttu-id="4ee72-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ee72-174">RELATED LINKS</span></span>

[<span data-ttu-id="4ee72-175">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ee72-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4ee72-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ee72-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4ee72-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ee72-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="4ee72-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ee72-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: db7d531b83dabe3bb5fc9dc79d86c3153d1553a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719399"
---
# <span data-ttu-id="5ecba-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ecba-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="5ecba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ecba-102">SYNOPSIS</span></span>
<span data-ttu-id="5ecba-103">Umożliwia utworzenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ecba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ecba-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-OutboundRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ecba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ecba-105">DESCRIPTION</span></span>
<span data-ttu-id="5ecba-106">Polecenie cmdlet **New-AzureRmLoadBalancer** umożliwia utworzenie modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ecba-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="5ecba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ecba-107">EXAMPLES</span></span>

### <span data-ttu-id="5ecba-108">Przykład 1. Tworzenie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="5ecba-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5ecba-109">Wdrożenie modułu równoważenia obciążenia wymaga wcześniejszego utworzenia kilku obiektów, a pierwsze siedem poleceń przedstawia sposób tworzenia tych obiektów.</span><span class="sxs-lookup"><span data-stu-id="5ecba-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="5ecba-110">Osiem poleceń powoduje utworzenie modułu równoważenia obciążenia o nazwie MyLoadBalancer w grupie zasób o nazwie moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ecba-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="5ecba-111">Dziewiąte i ostatnie polecenie otrzymuje nowe moduły równoważenia obciążenia w celu upewnienia się, że zostało pomyślnie utworzone.</span><span class="sxs-lookup"><span data-stu-id="5ecba-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="5ecba-112">Należy zauważyć, że w tym przykładzie przedstawiono tylko sposób tworzenia modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="5ecba-113">Musisz też skonfigurować go za pomocą polecenia cmdlet Add-AzureRmNetworkInterfaceIpConfig, aby przypisać karty sieciowe do różnych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5ecba-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="5ecba-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ecba-114">PARAMETERS</span></span>

### <span data-ttu-id="5ecba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ecba-115">-AsJob</span></span>
<span data-ttu-id="5ecba-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5ecba-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ecba-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ecba-117">-BackendAddressPool</span></span>
<span data-ttu-id="5ecba-118">Określa pulę adresów zaplecza, którą należy skojarzyć z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ecba-119">-DefaultProfile</span></span>
<span data-ttu-id="5ecba-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ecba-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ecba-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5ecba-121">-Force</span></span>
<span data-ttu-id="5ecba-122">Wskazuje, że to polecenie cmdlet powoduje utworzenie modułu równoważenia obciążenia nawet wtedy, gdy istnieje już moduł równoważenia obciążenia o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5ecba-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="5ecba-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ecba-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="5ecba-124">Określa listę zewnętrznych adresów IP, które należy skojarzyć z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecba-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="5ecba-125">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecba-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="5ecba-126">-InboundNatRule</span></span>
<span data-ttu-id="5ecba-127">Określa listę reguł translacji adresów sieciowych (NAT), które mają zostać skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecba-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="5ecba-128">-LoadBalancingRule</span></span>
<span data-ttu-id="5ecba-129">Określa listę reguł równoważenia obciążenia, które mają zostać skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecba-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5ecba-130">-Location</span></span>
<span data-ttu-id="5ecba-131">Określa region, w którym ma zostać utworzony moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="5ecba-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ecba-132">-Name</span></span>
<span data-ttu-id="5ecba-133">Określa nazwę tworzonego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-133">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="5ecba-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="5ecba-134">-OutboundRule</span></span>
<span data-ttu-id="5ecba-135">Reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="5ecba-135">The outbound rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecba-136">-Próbnik</span><span class="sxs-lookup"><span data-stu-id="5ecba-136">-Probe</span></span>
<span data-ttu-id="5ecba-137">Określa listę sondowań, które mają być skojarzone z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ecba-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ecba-138">-ResourceGroupName</span></span>
<span data-ttu-id="5ecba-139">Określa nazwę grupy zasobów, w której ma zostać utworzony moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="5ecba-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="5ecba-140">-Sku</span></span>
<span data-ttu-id="5ecba-141">Nazwa SKU modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ecba-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="5ecba-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ecba-142">-Tag</span></span>
<span data-ttu-id="5ecba-143">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5ecba-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5ecba-144">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5ecba-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5ecba-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ecba-145">-Confirm</span></span>
<span data-ttu-id="5ecba-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ecba-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ecba-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ecba-147">-WhatIf</span></span>
<span data-ttu-id="5ecba-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ecba-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ecba-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ecba-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ecba-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ecba-150">CommonParameters</span></span>
<span data-ttu-id="5ecba-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ecba-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ecba-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ecba-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ecba-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ecba-153">INPUTS</span></span>

### <span data-ttu-id="5ecba-154">System. String</span><span class="sxs-lookup"><span data-stu-id="5ecba-154">System.String</span></span>

### <span data-ttu-id="5ecba-155">System. Collections. Generic. list \` 1 [[Microsoft. Azure. Commands. Network. MODELES. PSFrontendIPConfiguration, Microsoft. Azure. Commands, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ecba-155">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="5ecba-156">System. Collections. Generic. list \` 1 [[Microsoft. Azure. Commands. Network. MODELES. PSBackendAddressPool, Microsoft. Azure. Commands, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ecba-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="5ecba-157">System. Collections. Generic. list \` 1 [[Microsoft. Azure. Commands. Network. MODELES. PSProbe, Microsoft. Azure. Commands, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ecba-157">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="5ecba-158">System. Collections. Generic. list \` 1 [[Microsoft. Azure. Commands. Network. MODELES. PSInboundNatRule, Microsoft. Azure. Commands, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ecba-158">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="5ecba-159">System. Collections. Generic. list \` 1 [[Microsoft. Azure. Commands. Network. MODELES. PSLoadBalancingRule, Microsoft. Azure. Commands, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ecba-159">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="5ecba-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5ecba-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5ecba-161">System. Collections. Generic. list \` 1 [[Microsoft. Azure. Commands. Network. MODELES. PSInboundNatPool, Microsoft. Azure. Commands, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ecba-161">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5ecba-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ecba-162">OUTPUTS</span></span>

### <span data-ttu-id="5ecba-163">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ecba-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5ecba-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ecba-164">NOTES</span></span>

## <span data-ttu-id="5ecba-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ecba-165">RELATED LINKS</span></span>

[<span data-ttu-id="5ecba-166">Dodaj-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ecba-166">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5ecba-167">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ecba-167">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="5ecba-168">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ecba-168">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="5ecba-169">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ecba-169">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

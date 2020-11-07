---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: daf136e5f0954aca32fce1c3f92f5ea5580dae16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869896"
---
# <span data-ttu-id="bc2ac-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc2ac-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="bc2ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2ac-103">Tworzy konfigurację adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="bc2ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc2ac-104">SYNTAX</span></span>

### <span data-ttu-id="bc2ac-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc2ac-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc2ac-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc2ac-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc2ac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bc2ac-107">DESCRIPTION</span></span>
<span data-ttu-id="bc2ac-108">Polecenie cmdlet **New-AzNetworkInterfaceIpConfig** umożliwia utworzenie konfiguracji adresu IP interfejsu sieci Azure dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="bc2ac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc2ac-109">EXAMPLES</span></span>

### <span data-ttu-id="bc2ac-110">1: Tworzenie konfiguracji adresu IP z publicznym adresem IP dla interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="bc2ac-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="bc2ac-111">Pierwsze dwa polecenia uzyskują sieć wirtualną o nazwie myvnet oraz podsieć, która została wcześniej utworzona.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="bc2ac-112">Są one przechowywane odpowiednio w $vnet i $Subnet.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="bc2ac-113">Trzecia komenda otrzymuje wcześniej utworzony publiczny adres IP o nazwie PIP1.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="bc2ac-114">Polecenie Dalej powoduje utworzenie nowej konfiguracji adresu IP o nazwie "IPConfig-1" jako podstawowej konfiguracji IP z skojarzonym publicznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="bc2ac-115">Następnie ostatnie polecenie tworzy interfejs sieciowy o nazwie mynic1 przy użyciu tej konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="bc2ac-116">2: Tworzenie konfiguracji adresu IP z prywatnym adresem IP</span><span class="sxs-lookup"><span data-stu-id="bc2ac-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="bc2ac-117">Pierwsze dwa polecenia uzyskują sieć wirtualną o nazwie myvnet oraz podsieć, która została wcześniej utworzona.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="bc2ac-118">Są one przechowywane odpowiednio w $vnet i $Subnet.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="bc2ac-119">W trzecim poleceniu jest tworzona nowa konfiguracja adresu IP o nazwie "IPConfig-2" z skojarzonym z nim prywatnym adresem IP 10.0.0.5.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="bc2ac-120">Następnie ostatnie polecenie tworzy interfejs sieciowy o nazwie mynic1 przy użyciu tej konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="bc2ac-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc2ac-121">PARAMETERS</span></span>

### <span data-ttu-id="bc2ac-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bc2ac-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="bc2ac-123">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bc2ac-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="bc2ac-125">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bc2ac-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="bc2ac-127">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bc2ac-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="bc2ac-129">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2ac-130">-DefaultProfile</span></span>
<span data-ttu-id="bc2ac-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc2ac-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bc2ac-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="bc2ac-133">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bc2ac-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="bc2ac-135">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="bc2ac-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="bc2ac-137">Określa kolekcję odwołań do zasad NAT dla ruchu przychodzącego modułu równoważenia obciążenia, do których należy ten element IPConfiguration interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="bc2ac-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="bc2ac-139">Określa kolekcję odwołań do reguł translacji adresów sieciowych (NAT) modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc2ac-140">-Name</span></span>
<span data-ttu-id="bc2ac-141">Określa nazwę konfiguracji adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="bc2ac-142">-Primary</span><span class="sxs-lookup"><span data-stu-id="bc2ac-142">-Primary</span></span>
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

### <span data-ttu-id="bc2ac-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc2ac-143">-PrivateIpAddress</span></span>
<span data-ttu-id="bc2ac-144">Określa statyczny adres IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-144">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="bc2ac-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="bc2ac-146">Określa wersję adresu IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="bc2ac-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bc2ac-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc2ac-148">Protokol</span><span class="sxs-lookup"><span data-stu-id="bc2ac-148">IPv4</span></span>
- <span data-ttu-id="bc2ac-149">Obsługi</span><span class="sxs-lookup"><span data-stu-id="bc2ac-149">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc2ac-150">-PublicIpAddress</span></span>
<span data-ttu-id="bc2ac-151">Określa obiekt **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="bc2ac-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="bc2ac-152">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bc2ac-153">-PublicIpAddressId</span></span>
<span data-ttu-id="bc2ac-154">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-155">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="bc2ac-155">-Subnet</span></span>
<span data-ttu-id="bc2ac-156">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="bc2ac-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="bc2ac-157">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bc2ac-158">-SubnetId</span></span>
<span data-ttu-id="bc2ac-159">Określa odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ac-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2ac-160">CommonParameters</span></span>
<span data-ttu-id="bc2ac-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc2ac-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2ac-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc2ac-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2ac-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc2ac-163">INPUTS</span></span>

### <span data-ttu-id="bc2ac-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="bc2ac-164">System.String[]</span></span>

### <span data-ttu-id="bc2ac-165">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="bc2ac-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="bc2ac-166">Microsoft. Azure. Commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="bc2ac-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="bc2ac-167">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="bc2ac-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="bc2ac-168">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="bc2ac-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="bc2ac-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc2ac-169">OUTPUTS</span></span>

### <span data-ttu-id="bc2ac-170">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc2ac-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="bc2ac-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc2ac-171">NOTES</span></span>
* <span data-ttu-id="bc2ac-172">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="bc2ac-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bc2ac-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc2ac-173">RELATED LINKS</span></span>

[<span data-ttu-id="bc2ac-174">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc2ac-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bc2ac-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc2ac-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bc2ac-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc2ac-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bc2ac-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc2ac-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)

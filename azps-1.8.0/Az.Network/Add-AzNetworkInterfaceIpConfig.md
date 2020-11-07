---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 587ae151830f4d4860aa90c25b80a799e1ba2946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709665"
---
# <span data-ttu-id="10df3-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10df3-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="10df3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10df3-102">SYNOPSIS</span></span>
<span data-ttu-id="10df3-103">Dodaje konfigurację adresu IP interfejsu sieciowego do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="10df3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10df3-104">SYNTAX</span></span>

### <span data-ttu-id="10df3-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10df3-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10df3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10df3-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10df3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="10df3-107">DESCRIPTION</span></span>
<span data-ttu-id="10df3-108">Polecenie cmdlet **Add-AzNetworkInterfaceIpConfig** umożliwia dodanie konfiguracji adresu IP interfejsu sieciowego do interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10df3-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="10df3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10df3-109">EXAMPLES</span></span>

### <span data-ttu-id="10df3-110">Przykład 1: Dodawanie nowej konfiguracji adresów IP przy użyciu grupy zabezpieczeń aplikacji</span><span class="sxs-lookup"><span data-stu-id="10df3-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="10df3-111">W tym przykładzie tworzymy nowy interfejs sieciowy MyNetworkInterface należący do podsieci w nowej MyVNET sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="10df3-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="10df3-112">Ponadto Utwórz pustą grupę zabezpieczeń aplikacji MyASG, aby skojarzyć ją z konfiguracjami IP w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="10df3-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="10df3-113">Po utworzeniu obu obiektów zostaje nałączona domyślna konfiguracja IP do obiektu MyASG.</span><span class="sxs-lookup"><span data-stu-id="10df3-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="10df3-114">W końcu Nowa konfiguracja adresów IP w interfejsie sieciowym jest również połączona z obiektem Grupa zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="10df3-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="10df3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10df3-115">PARAMETERS</span></span>

### <span data-ttu-id="10df3-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="10df3-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="10df3-117">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="10df3-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="10df3-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="10df3-119">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="10df3-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="10df3-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="10df3-121">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="10df3-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="10df3-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="10df3-123">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="10df3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10df3-124">-DefaultProfile</span></span>
<span data-ttu-id="10df3-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10df3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10df3-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="10df3-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="10df3-127">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="10df3-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="10df3-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="10df3-129">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="10df3-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="10df3-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="10df3-131">Określa kolekcję odwołań do reguł translacji adresów sieciowych (NAT) modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="10df3-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="10df3-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="10df3-133">Określa kolekcję odwołań do zasad ruchu przychodzącego NAT modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="10df3-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10df3-134">-Name</span></span>
<span data-ttu-id="10df3-135">Określa nazwę konfiguracji adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="10df3-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="10df3-136">-NetworkInterface</span></span>
<span data-ttu-id="10df3-137">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="10df3-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="10df3-138">To polecenie cmdlet umożliwia dodanie konfiguracji adresu IP interfejsu sieciowego do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="10df3-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10df3-139">-Primary</span><span class="sxs-lookup"><span data-stu-id="10df3-139">-Primary</span></span>
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

### <span data-ttu-id="10df3-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="10df3-140">-PrivateIpAddress</span></span>
<span data-ttu-id="10df3-141">Określa statyczny adres IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="10df3-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="10df3-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="10df3-143">Określa wersję adresu IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="10df3-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="10df3-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10df3-145">Protokol</span><span class="sxs-lookup"><span data-stu-id="10df3-145">IPv4</span></span>
- <span data-ttu-id="10df3-146">Obsługi</span><span class="sxs-lookup"><span data-stu-id="10df3-146">IPv6</span></span>

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

### <span data-ttu-id="10df3-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="10df3-147">-PublicIpAddress</span></span>
<span data-ttu-id="10df3-148">Określa obiekt **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="10df3-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="10df3-149">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="10df3-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="10df3-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="10df3-150">-PublicIpAddressId</span></span>
<span data-ttu-id="10df3-151">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="10df3-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="10df3-152">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="10df3-152">-Subnet</span></span>
<span data-ttu-id="10df3-153">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="10df3-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="10df3-154">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="10df3-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10df3-155">-SubnetId</span></span>
<span data-ttu-id="10df3-156">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="10df3-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="10df3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10df3-157">CommonParameters</span></span>
<span data-ttu-id="10df3-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10df3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10df3-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10df3-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10df3-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10df3-160">INPUTS</span></span>

### <span data-ttu-id="10df3-161">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="10df3-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="10df3-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="10df3-162">System.String[]</span></span>

### <span data-ttu-id="10df3-163">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="10df3-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="10df3-164">Microsoft. Azure. Commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="10df3-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="10df3-165">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="10df3-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="10df3-166">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="10df3-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="10df3-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10df3-167">OUTPUTS</span></span>

### <span data-ttu-id="10df3-168">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="10df3-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="10df3-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10df3-169">NOTES</span></span>
* <span data-ttu-id="10df3-170">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="10df3-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="10df3-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10df3-171">RELATED LINKS</span></span>

[<span data-ttu-id="10df3-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10df3-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="10df3-173">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10df3-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="10df3-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10df3-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="10df3-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10df3-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
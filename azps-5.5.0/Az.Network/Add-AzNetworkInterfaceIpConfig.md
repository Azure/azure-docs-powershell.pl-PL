---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9fef4a3cfe57b75ad992d4f4068bb0d51bbdcd90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241107"
---
# <span data-ttu-id="bdf70-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdf70-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="bdf70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdf70-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf70-103">Dodaje konfigurację protokołu IP interfejsu sieciowego do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="bdf70-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdf70-104">SYNTAX</span></span>

### <span data-ttu-id="bdf70-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="bdf70-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdf70-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bdf70-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdf70-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdf70-107">DESCRIPTION</span></span>
<span data-ttu-id="bdf70-108">Polecenie **cmdlet Add-AzNetworkInterfaceIpConfig** dodaje konfigurację adresu IP interfejsu sieciowego do interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf70-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="bdf70-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdf70-109">EXAMPLES</span></span>

### <span data-ttu-id="bdf70-110">Przykład 1. Dodawanie nowej konfiguracji adresu IP za pomocą grupy zabezpieczeń aplikacji</span><span class="sxs-lookup"><span data-stu-id="bdf70-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="bdf70-111">W tym przykładzie tworzymy nowy interfejs sieciowy MyNetworkInterface, który należy do podsieci w nowej sieci wirtualnej MyVNET.</span><span class="sxs-lookup"><span data-stu-id="bdf70-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="bdf70-112">Tworzymy również pustą grupę zabezpieczeń aplikacji, MyASG, aby skojarzyć z konfiguracjami adresów IP w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="bdf70-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="bdf70-113">Po utworzeniu obu obiektów łączymy domyślną konfigurację adresów IP z obiektem MyASG.</span><span class="sxs-lookup"><span data-stu-id="bdf70-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="bdf70-114">Na koniec tworzymy nową konfigurację adresów IP w interfejsie sieciowym połączonym również z obiektem grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bdf70-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="bdf70-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdf70-115">PARAMETERS</span></span>

### <span data-ttu-id="bdf70-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bdf70-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="bdf70-117">Określa zbiór odwołań puli adresów zaplecza bramy aplikacji, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bdf70-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bdf70-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="bdf70-119">Określa zbiór odwołań puli adresów zaplecza bramy aplikacji, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bdf70-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bdf70-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="bdf70-121">Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bdf70-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bdf70-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="bdf70-123">Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bdf70-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf70-124">-DefaultProfile</span></span>
<span data-ttu-id="bdf70-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf70-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdf70-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bdf70-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="bdf70-127">Określa zbiór odwołań puli adresów zaplecza równoważenia obciążenia, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bdf70-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bdf70-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="bdf70-129">Określa zbiór odwołań puli adresów zaplecza równoważenia obciążenia, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bdf70-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="bdf70-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="bdf70-131">Określa zbiór odwołań do reguł translacji adresów sieciowych (NAT, load balancer), do których należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bdf70-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="bdf70-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="bdf70-133">Określa zbiór odwołań do reguł przychodzącego serwera NAT dla równoważenia obciążenia, do których należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bdf70-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bdf70-134">-Name</span></span>
<span data-ttu-id="bdf70-135">Określa nazwę konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="bdf70-136">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdf70-136">-NetworkInterface</span></span>
<span data-ttu-id="bdf70-137">Określa **obiekt NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="bdf70-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="bdf70-138">To polecenie cmdlet dodaje konfigurację protokołu IP interfejsu sieciowego do obiektu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bdf70-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdf70-139">— podstawowy</span><span class="sxs-lookup"><span data-stu-id="bdf70-139">-Primary</span></span>
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

### <span data-ttu-id="bdf70-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf70-140">-PrivateIpAddress</span></span>
<span data-ttu-id="bdf70-141">Określa statyczny adres IP konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="bdf70-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="bdf70-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="bdf70-143">Określa wersję adresu IP konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="bdf70-144">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bdf70-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bdf70-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="bdf70-145">IPv4</span></span>
- <span data-ttu-id="bdf70-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="bdf70-146">IPv6</span></span>

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

### <span data-ttu-id="bdf70-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf70-147">-PublicIpAddress</span></span>
<span data-ttu-id="bdf70-148">Określa obiekt **PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="bdf70-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="bdf70-149">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, który należy skojarzyć z tą konfiguracją adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="bdf70-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bdf70-150">-PublicIpAddressId</span></span>
<span data-ttu-id="bdf70-151">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, który należy skojarzyć z tą konfiguracją adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="bdf70-152">-Subnet</span><span class="sxs-lookup"><span data-stu-id="bdf70-152">-Subnet</span></span>
<span data-ttu-id="bdf70-153">Określa obiekt **Podsieci.**</span><span class="sxs-lookup"><span data-stu-id="bdf70-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="bdf70-154">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="bdf70-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bdf70-155">-SubnetId</span></span>
<span data-ttu-id="bdf70-156">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdf70-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="bdf70-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf70-157">CommonParameters</span></span>
<span data-ttu-id="bdf70-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf70-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf70-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdf70-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf70-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdf70-160">INPUTS</span></span>

### <span data-ttu-id="bdf70-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdf70-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="bdf70-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bdf70-162">System.String[]</span></span>

### <span data-ttu-id="bdf70-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="bdf70-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="bdf70-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="bdf70-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="bdf70-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="bdf70-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="bdf70-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="bdf70-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="bdf70-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bdf70-167">OUTPUTS</span></span>

### <span data-ttu-id="bdf70-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdf70-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="bdf70-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdf70-169">NOTES</span></span>
* <span data-ttu-id="bdf70-170">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="bdf70-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bdf70-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdf70-171">RELATED LINKS</span></span>

[<span data-ttu-id="bdf70-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdf70-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bdf70-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdf70-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bdf70-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdf70-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bdf70-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdf70-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)

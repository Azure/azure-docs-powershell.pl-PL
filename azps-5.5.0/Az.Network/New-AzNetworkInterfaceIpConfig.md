---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202795"
---
# <span data-ttu-id="3ad9c-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ad9c-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="3ad9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ad9c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad9c-103">Tworzy konfigurację protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="3ad9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3ad9c-104">SYNTAX</span></span>

### <span data-ttu-id="3ad9c-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="3ad9c-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ad9c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad9c-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ad9c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3ad9c-107">DESCRIPTION</span></span>
<span data-ttu-id="3ad9c-108">Polecenie **cmdlet New-AzNetworkInterfaceIpConfig** tworzy konfigurację adresu IP interfejsu sieciowego platformy Azure dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="3ad9c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3ad9c-109">EXAMPLES</span></span>

### <span data-ttu-id="3ad9c-110">1. Tworzenie konfiguracji adresu IP z publicznym adresem IP dla interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="3ad9c-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="3ad9c-111">Pierwsze dwa polecenia otrzymają utworzoną wcześniej sieć wirtualną o nazwie myvnet i podsieć o nazwie mysubnet.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="3ad9c-112">Są one przechowywane odpowiednio $vnet $Subnet danych.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="3ad9c-113">Trzecie polecenie otrzymuje utworzony wcześniej publiczny adres IP o nazwie PIP1.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="3ad9c-114">Polecenie Forth tworzy nową konfigurację protokołu IP o nazwie "IPConfig-1" jako podstawową konfigurację adresu IP z skojarzonym z nim publicznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="3ad9c-115">Ostatnie polecenie tworzy wówczas interfejs sieciowy o nazwie mynic1 przy użyciu tej konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="3ad9c-116">2. Tworzenie konfiguracji adresu IP przy użyciu prywatnego adresu IP</span><span class="sxs-lookup"><span data-stu-id="3ad9c-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="3ad9c-117">Pierwsze dwa polecenia otrzymają utworzoną wcześniej sieć wirtualną o nazwie myvnet i podsieć o nazwie mysubnet.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="3ad9c-118">Są one przechowywane odpowiednio $vnet $Subnet danych.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="3ad9c-119">Trzecie polecenie tworzy nową konfigurację adresów IP o nazwie "IPConfig-2" z skojarzonym z nim prywatnym adresem IP 10.0.0.5.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="3ad9c-120">Ostatnie polecenie tworzy wówczas interfejs sieciowy o nazwie mynic1 przy użyciu tej konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="3ad9c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ad9c-121">PARAMETERS</span></span>

### <span data-ttu-id="3ad9c-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ad9c-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="3ad9c-123">Określa zbiór odwołań puli adresów zaplecza bramy aplikacji, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3ad9c-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3ad9c-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="3ad9c-125">Określa zbiór odwołań puli adresów zaplecza bramy aplikacji, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3ad9c-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3ad9c-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="3ad9c-127">Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3ad9c-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3ad9c-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="3ad9c-129">Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3ad9c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad9c-130">-DefaultProfile</span></span>
<span data-ttu-id="3ad9c-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ad9c-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ad9c-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="3ad9c-133">Określa zbiór odwołań puli adresów zaplecza równoważenia obciążenia, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3ad9c-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3ad9c-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="3ad9c-135">Określa zbiór odwołań puli adresów zaplecza równoważenia obciążenia, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3ad9c-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="3ad9c-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="3ad9c-137">Określa zbiór odwołań reguły przychodzącej do reguły nat równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="3ad9c-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="3ad9c-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="3ad9c-139">Określa zbiór odwołań do reguł translacji adresów sieciowych (NAT, load balancer), do których należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="3ad9c-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3ad9c-140">-Name</span></span>
<span data-ttu-id="3ad9c-141">Określa nazwę konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="3ad9c-142">— podstawowy</span><span class="sxs-lookup"><span data-stu-id="3ad9c-142">-Primary</span></span>
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

### <span data-ttu-id="3ad9c-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3ad9c-143">-PrivateIpAddress</span></span>
<span data-ttu-id="3ad9c-144">Określa statyczny adres IP konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="3ad9c-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="3ad9c-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="3ad9c-146">Określa wersję adresu IP konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="3ad9c-147">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3ad9c-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ad9c-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="3ad9c-148">IPv4</span></span>
- <span data-ttu-id="3ad9c-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="3ad9c-149">IPv6</span></span>

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

### <span data-ttu-id="3ad9c-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3ad9c-150">-PublicIpAddress</span></span>
<span data-ttu-id="3ad9c-151">Określa obiekt **PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="3ad9c-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="3ad9c-152">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, który należy skojarzyć z tą konfiguracją adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="3ad9c-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3ad9c-153">-PublicIpAddressId</span></span>
<span data-ttu-id="3ad9c-154">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, który należy skojarzyć z tą konfiguracją adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="3ad9c-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3ad9c-155">-Subnet</span></span>
<span data-ttu-id="3ad9c-156">Określa obiekt **Podsieci.**</span><span class="sxs-lookup"><span data-stu-id="3ad9c-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="3ad9c-157">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="3ad9c-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3ad9c-158">-SubnetId</span></span>
<span data-ttu-id="3ad9c-159">Określa odwołanie do podsieci, w której jest tworzona ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="3ad9c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad9c-160">CommonParameters</span></span>
<span data-ttu-id="3ad9c-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad9c-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad9c-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad9c-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ad9c-163">INPUTS</span></span>

### <span data-ttu-id="3ad9c-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3ad9c-164">System.String[]</span></span>

### <span data-ttu-id="3ad9c-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="3ad9c-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="3ad9c-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="3ad9c-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="3ad9c-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="3ad9c-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="3ad9c-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="3ad9c-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="3ad9c-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ad9c-169">OUTPUTS</span></span>

### <span data-ttu-id="3ad9c-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ad9c-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="3ad9c-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3ad9c-171">NOTES</span></span>
* <span data-ttu-id="3ad9c-172">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="3ad9c-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3ad9c-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ad9c-173">RELATED LINKS</span></span>

[<span data-ttu-id="3ad9c-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ad9c-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3ad9c-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ad9c-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3ad9c-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ad9c-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3ad9c-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ad9c-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)

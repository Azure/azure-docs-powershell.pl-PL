---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9427a79c607d56fcc9ce7a39fa24bfa3e301cfc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003386"
---
# <span data-ttu-id="7df19-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7df19-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="7df19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7df19-102">SYNOPSIS</span></span>
<span data-ttu-id="7df19-103">Aktualizuje konfigurację protokołu IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="7df19-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7df19-104">SYNTAX</span></span>

### <span data-ttu-id="7df19-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7df19-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7df19-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7df19-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7df19-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7df19-107">DESCRIPTION</span></span>
<span data-ttu-id="7df19-108">Polecenie **cmdlet Set-AzNetworkInterfaceIpConfig** aktualizuje konfigurację protokołu IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="7df19-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7df19-109">EXAMPLES</span></span>

### <span data-ttu-id="7df19-110">1. Zmienianie adresu IP konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="7df19-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7df19-111">Pierwsze dwa polecenia otrzymają wirtualną sieć o nazwie myvnet i podsieci o nazwie mysubnet i przechowują ją w zmiennych $vnet i $subnet.</span><span class="sxs-lookup"><span data-stu-id="7df19-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="7df19-112">Trzecie polecenie pobiera interfejs sieciowy nic1 skojarzony z konfiguracją protokołu IP, która wymaga aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7df19-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="7df19-113">Trzecie polecenie ustawia prywatny adres IP podstawowej konfiguracji ipconfig1 na 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="7df19-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="7df19-114">Ostatnie polecenie aktualizuje interfejs sieciowy, upewniając się, że zmiany zostały wprowadzone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="7df19-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="7df19-115">2. Kojarzenie konfiguracji protokołu IP z grupą zabezpieczeń aplikacji</span><span class="sxs-lookup"><span data-stu-id="7df19-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7df19-116">W tym przykładzie zmienna, $asg zawiera odwołanie do grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7df19-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="7df19-117">Czwarte polecenie pobiera interfejs sieciowy nic1 skojarzony z konfiguracją protokołu IP, która wymaga aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7df19-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="7df19-118">Ta Set-AzNetworkInterfaceIpConfig ustawia prywatny adres IP podstawowej konfiguracji ipconfig1 na 10.0.0.11 i tworzy skojarzenie z pobraną grupą zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7df19-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="7df19-119">Ostatnie polecenie aktualizuje interfejs sieciowy, upewniając się, że zmiany zostały wprowadzone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="7df19-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="7df19-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7df19-120">PARAMETERS</span></span>

### <span data-ttu-id="7df19-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7df19-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="7df19-122">Określa zbiór odwołań puli adresów zaplecza bramy aplikacji, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7df19-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7df19-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="7df19-124">Określa zbiór odwołań puli adresów zaplecza bramy aplikacji, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7df19-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7df19-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="7df19-126">Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7df19-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7df19-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="7df19-128">Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7df19-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df19-129">-DefaultProfile</span></span>
<span data-ttu-id="7df19-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7df19-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7df19-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7df19-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="7df19-132">Określa zbiór odwołań puli adresów zaplecza równoważenia obciążenia, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7df19-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7df19-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="7df19-134">Określa zbiór odwołań puli adresów zaplecza równoważenia obciążenia, do której należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7df19-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="7df19-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="7df19-136">Określa zbiór odwołań do reguł translacji adresów sieciowych (NAT), do których należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7df19-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="7df19-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="7df19-138">Określa zbiór odwołań do reguł nat ruchu przychodzącego NAT równoważenia obciążenia, do których należy ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7df19-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7df19-139">-Name</span></span>
<span data-ttu-id="7df19-140">Określa nazwę konfiguracji sieciowego adresu IP, dla której jest ustawiane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7df19-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="7df19-141">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7df19-141">-NetworkInterface</span></span>
<span data-ttu-id="7df19-142">Określa **obiekt NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="7df19-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="7df19-143">To polecenie cmdlet dodaje konfigurację protokołu IP interfejsu sieciowego do obiektu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7df19-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="7df19-144">— podstawowy</span><span class="sxs-lookup"><span data-stu-id="7df19-144">-Primary</span></span>
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

### <span data-ttu-id="7df19-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7df19-145">-PrivateIpAddress</span></span>
<span data-ttu-id="7df19-146">Określa statyczny adres IP konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="7df19-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7df19-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7df19-148">Określa wersję adresu IP konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="7df19-149">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7df19-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7df19-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="7df19-150">IPv4</span></span>
- <span data-ttu-id="7df19-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="7df19-151">IPv6</span></span>

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

### <span data-ttu-id="7df19-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7df19-152">-PublicIpAddress</span></span>
<span data-ttu-id="7df19-153">Określa obiekt **PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="7df19-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="7df19-154">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, który należy skojarzyć z tą konfiguracją adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7df19-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7df19-155">-PublicIpAddressId</span></span>
<span data-ttu-id="7df19-156">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, który należy skojarzyć z tą konfiguracją adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7df19-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7df19-157">-Subnet</span></span>
<span data-ttu-id="7df19-158">Określa obiekt **Podsieci.**</span><span class="sxs-lookup"><span data-stu-id="7df19-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="7df19-159">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7df19-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7df19-160">-SubnetId</span></span>
<span data-ttu-id="7df19-161">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona ta konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7df19-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7df19-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df19-162">CommonParameters</span></span>
<span data-ttu-id="7df19-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df19-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df19-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df19-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df19-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7df19-165">INPUTS</span></span>

### <span data-ttu-id="7df19-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7df19-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="7df19-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7df19-167">System.String[]</span></span>

### <span data-ttu-id="7df19-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="7df19-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="7df19-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="7df19-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="7df19-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="7df19-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="7df19-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="7df19-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="7df19-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7df19-172">OUTPUTS</span></span>

### <span data-ttu-id="7df19-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7df19-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7df19-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7df19-174">NOTES</span></span>
* <span data-ttu-id="7df19-175">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="7df19-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7df19-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7df19-176">RELATED LINKS</span></span>

[<span data-ttu-id="7df19-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7df19-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7df19-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7df19-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7df19-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7df19-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7df19-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7df19-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

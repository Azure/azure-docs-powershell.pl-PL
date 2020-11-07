---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0b6c0c850f389dba27e483f5de4e4aee1fca7450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708959"
---
# <span data-ttu-id="bc66f-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc66f-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="bc66f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc66f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc66f-103">Umożliwia zaktualizowanie konfiguracji IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="bc66f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc66f-104">SYNTAX</span></span>

### <span data-ttu-id="bc66f-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc66f-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc66f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc66f-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc66f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bc66f-107">DESCRIPTION</span></span>
<span data-ttu-id="bc66f-108">Polecenie cmdlet **Set-AzNetworkInterfaceIpConfig** AKTUALIZUJE konfigurację IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="bc66f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc66f-109">EXAMPLES</span></span>

### <span data-ttu-id="bc66f-110">1: Zmienianie adresu IP konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="bc66f-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="bc66f-111">Pierwsze dwa polecenia uzyskują sieć wirtualną o nazwie myvnet oraz podsieć, a następnie przechowują ją w $vnet zmiennych i $subnet.</span><span class="sxs-lookup"><span data-stu-id="bc66f-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="bc66f-112">Trzecia komenda uzyskuje interfejs sieciowy NIC1 skojarzony z konfiguracją IP, która musi zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="bc66f-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="bc66f-113">Trzecie polecenie ustawia prywatny adres IP ipconfig1 podstawowej konfiguracji IP na 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="bc66f-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="bc66f-114">Na koniec ostatnie polecenie aktualizuje interfejs sieciowy, dzięki czemu zmiany zostały wprowadzone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="bc66f-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="bc66f-115">2: Kojarzenie konfiguracji IP z grupą zabezpieczeń aplikacji</span><span class="sxs-lookup"><span data-stu-id="bc66f-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="bc66f-116">W tym przykładzie zmienna $asg zawiera odwołanie do grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc66f-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="bc66f-117">W czwartym poleceniu jest pobierany interfejs sieciowy NIC1 skojarzony z konfiguracją IP, która musi zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="bc66f-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="bc66f-118">Set-AzNetworkInterfaceIpConfig służy do ustawiania prywatnego adresu IP ipconfig1 podstawowej konfiguracji IP na 10.0.0.11 i tworzenia skojarzenia z pobraną grupą zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc66f-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="bc66f-119">Na koniec ostatnie polecenie aktualizuje interfejs sieciowy, dzięki czemu zmiany zostały wprowadzone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="bc66f-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="bc66f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc66f-120">PARAMETERS</span></span>

### <span data-ttu-id="bc66f-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bc66f-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="bc66f-122">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bc66f-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bc66f-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="bc66f-124">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bc66f-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bc66f-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="bc66f-126">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bc66f-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bc66f-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="bc66f-128">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bc66f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc66f-129">-DefaultProfile</span></span>
<span data-ttu-id="bc66f-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc66f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc66f-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bc66f-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="bc66f-132">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bc66f-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bc66f-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="bc66f-134">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bc66f-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="bc66f-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="bc66f-136">Określa kolekcję odwołań do reguł translacji adresów sieciowych (NAT) modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bc66f-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="bc66f-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="bc66f-138">Określa kolekcję odwołań do zasad ruchu przychodzącego NAT modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="bc66f-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc66f-139">-Name</span></span>
<span data-ttu-id="bc66f-140">Określa nazwę konfiguracji sieci IP, dla której ustawiono to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc66f-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="bc66f-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bc66f-141">-NetworkInterface</span></span>
<span data-ttu-id="bc66f-142">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="bc66f-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="bc66f-143">To polecenie cmdlet umożliwia dodanie konfiguracji adresu IP interfejsu sieciowego do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bc66f-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc66f-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="bc66f-144">-Primary</span></span>
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

### <span data-ttu-id="bc66f-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc66f-145">-PrivateIpAddress</span></span>
<span data-ttu-id="bc66f-146">Określa statyczny adres IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="bc66f-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="bc66f-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="bc66f-148">Określa wersję adresu IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="bc66f-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bc66f-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc66f-150">Protokol</span><span class="sxs-lookup"><span data-stu-id="bc66f-150">IPv4</span></span>
- <span data-ttu-id="bc66f-151">Obsługi</span><span class="sxs-lookup"><span data-stu-id="bc66f-151">IPv6</span></span>

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

### <span data-ttu-id="bc66f-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc66f-152">-PublicIpAddress</span></span>
<span data-ttu-id="bc66f-153">Określa obiekt **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="bc66f-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="bc66f-154">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="bc66f-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="bc66f-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bc66f-155">-PublicIpAddressId</span></span>
<span data-ttu-id="bc66f-156">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="bc66f-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="bc66f-157">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="bc66f-157">-Subnet</span></span>
<span data-ttu-id="bc66f-158">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="bc66f-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="bc66f-159">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="bc66f-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bc66f-160">-SubnetId</span></span>
<span data-ttu-id="bc66f-161">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bc66f-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="bc66f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc66f-162">CommonParameters</span></span>
<span data-ttu-id="bc66f-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc66f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc66f-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc66f-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc66f-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc66f-165">INPUTS</span></span>

### <span data-ttu-id="bc66f-166">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bc66f-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="bc66f-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="bc66f-167">System.String[]</span></span>

### <span data-ttu-id="bc66f-168">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="bc66f-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="bc66f-169">Microsoft. Azure. Commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="bc66f-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="bc66f-170">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="bc66f-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="bc66f-171">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="bc66f-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="bc66f-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc66f-172">OUTPUTS</span></span>

### <span data-ttu-id="bc66f-173">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bc66f-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="bc66f-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc66f-174">NOTES</span></span>
* <span data-ttu-id="bc66f-175">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="bc66f-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bc66f-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc66f-176">RELATED LINKS</span></span>

[<span data-ttu-id="bc66f-177">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc66f-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bc66f-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc66f-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bc66f-179">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc66f-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bc66f-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc66f-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0e74aa06d2966ed4e907de7428ddc1f4d3a6f2cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892762"
---
# <span data-ttu-id="3f6f6-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f6f6-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="3f6f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6f6-103">Ustawia stan celu konfiguracji adresu IP interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="3f6f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f6f6-104">SYNTAX</span></span>

### <span data-ttu-id="3f6f6-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3f6f6-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f6f6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6f6-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f6f6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3f6f6-107">DESCRIPTION</span></span>
<span data-ttu-id="3f6f6-108">Polecenie cmdlet **Set-AzNetworkInterfaceIpConfig** ustawia stan celu konfiguracji protokołu IP interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="3f6f6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f6f6-109">EXAMPLES</span></span>

### <span data-ttu-id="3f6f6-110">1: Zmienianie adresu IP konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="3f6f6-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="3f6f6-111">Pierwsze dwa polecenia uzyskują sieć wirtualną o nazwie myvnet oraz podsieć, a następnie przechowują ją w $vnet zmiennych i $subnet.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="3f6f6-112">Trzecia komenda uzyskuje interfejs sieciowy NIC1 skojarzony z konfiguracją IP, która musi zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="3f6f6-113">Trzecie polecenie ustawia prywatny adres IP ipconfig1 podstawowej konfiguracji IP na 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="3f6f6-114">Na koniec ostatnie polecenie aktualizuje interfejs sieciowy, dzięki czemu zmiany zostały wprowadzone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="3f6f6-115">2: Kojarzenie konfiguracji adresów IP z aplikacją Application Security groupp</span><span class="sxs-lookup"><span data-stu-id="3f6f6-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="3f6f6-116">W tym przykładzie zmienna $asg zawiera odwołanie do grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="3f6f6-117">W czwartym poleceniu jest pobierany interfejs sieciowy NIC1 skojarzony z konfiguracją IP, która musi zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="3f6f6-118">Set-AzNetworkInterfaceIpConfig służy do ustawiania prywatnego adresu IP ipconfig1 podstawowej konfiguracji IP na 10.0.0.11 i tworzenia skojarzenia z pobraną grupą zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="3f6f6-119">Na koniec ostatnie polecenie aktualizuje interfejs sieciowy, dzięki czemu zmiany zostały wprowadzone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="3f6f6-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f6f6-120">PARAMETERS</span></span>

### <span data-ttu-id="3f6f6-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f6f6-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="3f6f6-122">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3f6f6-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="3f6f6-124">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3f6f6-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="3f6f6-126">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3f6f6-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="3f6f6-128">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6f6-129">-DefaultProfile</span></span>
<span data-ttu-id="3f6f6-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f6f6-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="3f6f6-132">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3f6f6-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="3f6f6-134">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="3f6f6-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="3f6f6-136">Określa kolekcję odwołań do reguł translacji adresów sieciowych (NAT) modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="3f6f6-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="3f6f6-138">Określa kolekcję odwołań do zasad ruchu przychodzącego NAT modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f6f6-139">-Name</span></span>
<span data-ttu-id="3f6f6-140">Określa nazwę konfiguracji sieci IP, dla której ustawiono to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3f6f6-141">-NetworkInterface</span></span>
<span data-ttu-id="3f6f6-142">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="3f6f6-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="3f6f6-143">To polecenie cmdlet umożliwia dodanie konfiguracji adresu IP interfejsu sieciowego do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="3f6f6-144">-Primary</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f6f6-145">-PrivateIpAddress</span></span>
<span data-ttu-id="3f6f6-146">Określa statyczny adres IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-146">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="3f6f6-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="3f6f6-148">Określa wersję adresu IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="3f6f6-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3f6f6-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f6f6-150">Protokol</span><span class="sxs-lookup"><span data-stu-id="3f6f6-150">IPv4</span></span>
- <span data-ttu-id="3f6f6-151">Obsługi</span><span class="sxs-lookup"><span data-stu-id="3f6f6-151">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f6f6-152">-PublicIpAddress</span></span>
<span data-ttu-id="3f6f6-153">Określa obiekt **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="3f6f6-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="3f6f6-154">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3f6f6-155">-PublicIpAddressId</span></span>
<span data-ttu-id="3f6f6-156">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-157">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="3f6f6-157">-Subnet</span></span>
<span data-ttu-id="3f6f6-158">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="3f6f6-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="3f6f6-159">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3f6f6-160">-SubnetId</span></span>
<span data-ttu-id="3f6f6-161">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6f6-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6f6-162">CommonParameters</span></span>
<span data-ttu-id="3f6f6-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f6f6-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6f6-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f6f6-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6f6-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f6f6-165">INPUTS</span></span>

### <span data-ttu-id="3f6f6-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3f6f6-166">PSNetworkInterface</span></span>
<span data-ttu-id="3f6f6-167">Parametr "NetworkInterface" akceptuje wartość typu "PSNetworkInterface" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3f6f6-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="3f6f6-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f6f6-168">OUTPUTS</span></span>

### <span data-ttu-id="3f6f6-169">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3f6f6-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="3f6f6-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f6f6-170">NOTES</span></span>
* <span data-ttu-id="3f6f6-171">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="3f6f6-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3f6f6-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f6f6-172">RELATED LINKS</span></span>

[<span data-ttu-id="3f6f6-173">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f6f6-173">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3f6f6-174">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f6f6-174">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3f6f6-175">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f6f6-175">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3f6f6-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f6f6-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)



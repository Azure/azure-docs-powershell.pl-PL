---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 6bf01750543fa5564e9490ad85d84cc258f10f4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716901"
---
# <span data-ttu-id="fbb8d-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbb8d-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="fbb8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbb8d-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb8d-103">Ustawia stan celu konfiguracji adresu IP interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbb8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbb8d-104">SYNTAX</span></span>

### <span data-ttu-id="fbb8d-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fbb8d-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbb8d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbb8d-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbb8d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fbb8d-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb8d-108">Polecenie cmdlet **Set-AzureRmNetworkInterfaceIpConfig** ustawia stan celu konfiguracji protokołu IP interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="fbb8d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbb8d-109">EXAMPLES</span></span>

### <span data-ttu-id="fbb8d-110">1: Zmienianie adresu IP konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="fbb8d-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="fbb8d-111">Pierwsze dwa polecenia uzyskują sieć wirtualną o nazwie myvnet oraz podsieć, a następnie przechowują ją w $vnet zmiennych i $subnet.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="fbb8d-112">Trzecia komenda uzyskuje interfejs sieciowy NIC1 skojarzony z konfiguracją IP, która musi zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="fbb8d-113">Trzecie polecenie ustawia prywatny adres IP ipconfig1 podstawowej konfiguracji IP na 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="fbb8d-114">Na koniec ostatnie polecenie aktualizuje interfejs sieciowy, dzięki czemu zmiany zostały wprowadzone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="fbb8d-115">2: Kojarzenie konfiguracji adresów IP z aplikacją Application Security groupp</span><span class="sxs-lookup"><span data-stu-id="fbb8d-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="fbb8d-116">W tym przykładzie zmienna $asg zawiera odwołanie do grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="fbb8d-117">W czwartym poleceniu jest pobierany interfejs sieciowy NIC1 skojarzony z konfiguracją IP, która musi zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="fbb8d-118">Set-AzureRmNetworkInterfaceIpConfig służy do ustawiania prywatnego adresu IP ipconfig1 podstawowej konfiguracji IP na 10.0.0.11 i tworzenia skojarzenia z pobraną grupą zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="fbb8d-119">Na koniec ostatnie polecenie aktualizuje interfejs sieciowy, dzięki czemu zmiany zostały wprowadzone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="fbb8d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbb8d-120">PARAMETERS</span></span>

### <span data-ttu-id="fbb8d-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fbb8d-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="fbb8d-122">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="fbb8d-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="fbb8d-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="fbb8d-124">Określa kolekcję odwołań puli adresów zaplecza bramy Application Gateway, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="fbb8d-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fbb8d-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="fbb8d-126">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="fbb8d-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fbb8d-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="fbb8d-128">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="fbb8d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb8d-129">-DefaultProfile</span></span>
<span data-ttu-id="fbb8d-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbb8d-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fbb8d-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="fbb8d-132">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="fbb8d-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="fbb8d-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="fbb8d-134">Określa kolekcję odwołań do puli adresów zaplecza modułu równoważenia obciążenia, do której należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="fbb8d-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="fbb8d-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="fbb8d-136">Określa kolekcję odwołań do reguł translacji adresów sieciowych (NAT) modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="fbb8d-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="fbb8d-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="fbb8d-138">Określa kolekcję odwołań do zasad ruchu przychodzącego NAT modułu równoważenia obciążenia, do których należy ta konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="fbb8d-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fbb8d-139">-Name</span></span>
<span data-ttu-id="fbb8d-140">Określa nazwę konfiguracji sieci IP, dla której ustawiono to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="fbb8d-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fbb8d-141">-NetworkInterface</span></span>
<span data-ttu-id="fbb8d-142">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="fbb8d-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="fbb8d-143">To polecenie cmdlet umożliwia dodanie konfiguracji adresu IP interfejsu sieciowego do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbb8d-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="fbb8d-144">-Primary</span></span>
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

### <span data-ttu-id="fbb8d-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="fbb8d-145">-PrivateIpAddress</span></span>
<span data-ttu-id="fbb8d-146">Określa statyczny adres IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="fbb8d-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="fbb8d-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="fbb8d-148">Określa wersję adresu IP konfiguracji IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="fbb8d-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fbb8d-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fbb8d-150">Protokol</span><span class="sxs-lookup"><span data-stu-id="fbb8d-150">IPv4</span></span>
- <span data-ttu-id="fbb8d-151">Obsługi</span><span class="sxs-lookup"><span data-stu-id="fbb8d-151">IPv6</span></span>

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

### <span data-ttu-id="fbb8d-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fbb8d-152">-PublicIpAddress</span></span>
<span data-ttu-id="fbb8d-153">Określa obiekt **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="fbb8d-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="fbb8d-154">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="fbb8d-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="fbb8d-155">-PublicIpAddressId</span></span>
<span data-ttu-id="fbb8d-156">To polecenie cmdlet tworzy odwołanie do publicznego adresu IP, które ma zostać skojarzone z tą konfiguracją interfejsu sieciowego IP.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="fbb8d-157">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="fbb8d-157">-Subnet</span></span>
<span data-ttu-id="fbb8d-158">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="fbb8d-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="fbb8d-159">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="fbb8d-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fbb8d-160">-SubnetId</span></span>
<span data-ttu-id="fbb8d-161">To polecenie cmdlet tworzy odwołanie do podsieci, w której jest tworzona Konfiguracja adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="fbb8d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb8d-162">CommonParameters</span></span>
<span data-ttu-id="fbb8d-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb8d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb8d-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb8d-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb8d-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbb8d-165">INPUTS</span></span>

### <span data-ttu-id="fbb8d-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fbb8d-166">PSNetworkInterface</span></span>
<span data-ttu-id="fbb8d-167">Parametr "NetworkInterface" akceptuje wartość typu "PSNetworkInterface" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="fbb8d-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="fbb8d-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbb8d-168">OUTPUTS</span></span>

### <span data-ttu-id="fbb8d-169">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fbb8d-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="fbb8d-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbb8d-170">NOTES</span></span>
* <span data-ttu-id="fbb8d-171">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="fbb8d-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fbb8d-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbb8d-172">RELATED LINKS</span></span>

[<span data-ttu-id="fbb8d-173">Dodaj-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbb8d-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fbb8d-174">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbb8d-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fbb8d-175">Nowe — AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbb8d-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fbb8d-176">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbb8d-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501255"
---
# <span data-ttu-id="6ee29-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ee29-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="6ee29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ee29-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee29-103">Tworzy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="6ee29-103">Creates a network interface.</span></span>

## <span data-ttu-id="6ee29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ee29-104">SYNTAX</span></span>

### <span data-ttu-id="6ee29-105">SetByIpConfigurationResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ee29-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ee29-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6ee29-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ee29-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ee29-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ee29-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6ee29-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ee29-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6ee29-109">DESCRIPTION</span></span>
<span data-ttu-id="6ee29-110">Polecenie cmdlet **New-AzNetworkInterface** tworzy interfejs sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee29-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="6ee29-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ee29-111">EXAMPLES</span></span>

### <span data-ttu-id="6ee29-112">Przykład 1. Tworzenie interfejsu sieciowego platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6ee29-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="6ee29-113">To polecenie tworzy interfejs sieciowy o nazwie NetworkInterface001 z dynamicznie przydzielonym prywatnym adresem IP z Subnet1 w sieci wirtualnej o nazwie VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="6ee29-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="6ee29-114">Polecenie powoduje również przypisanie dwóch serwerów DNS do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="6ee29-115">Podrzędny zasób elementu IPConfiguration zostanie utworzony automatycznie przy użyciu nazwy IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="6ee29-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="6ee29-116">Przykład 2: Tworzenie interfejsu sieciowego platformy Azure przy użyciu obiektu konfiguracji IP</span><span class="sxs-lookup"><span data-stu-id="6ee29-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="6ee29-117">W tym przykładzie przedstawiono tworzenie nowego interfejsu sieciowego za pomocą obiektu konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="6ee29-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="6ee29-118">Obiekt konfiguracji IP określa statyczny prywatny adres IPv4.</span><span class="sxs-lookup"><span data-stu-id="6ee29-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="6ee29-119">Pierwsze polecenie pobiera istniejącą określoną sieć wirtualną, która jest używana do przypisania podsieci w drugim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="6ee29-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="6ee29-120">Drugie polecenie tworzy konfigurację adresu IP interfejsu sieciowego o nazwie IPConfig1 i zapisuje konfigurację w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="6ee29-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="6ee29-121">Trzecia komenda tworzy interfejs sieciowy o nazwie NetworkInterface1, w którym jest używana konfiguracja IP interfejsu sieciowego przechowywana w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="6ee29-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="6ee29-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6ee29-122">Example 3</span></span>

<span data-ttu-id="6ee29-123">Tworzy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="6ee29-123">Creates a network interface.</span></span> <span data-ttu-id="6ee29-124">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="6ee29-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="6ee29-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ee29-125">PARAMETERS</span></span>

### <span data-ttu-id="6ee29-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6ee29-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="6ee29-127">Określa obiekt **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="6ee29-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="6ee29-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6ee29-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="6ee29-129">Określa identyfikator obiektu **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="6ee29-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="6ee29-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6ee29-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="6ee29-131">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których powinna należeć Konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="6ee29-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6ee29-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="6ee29-133">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których powinna należeć Konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="6ee29-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ee29-134">-AsJob</span></span>
<span data-ttu-id="6ee29-135">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6ee29-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ee29-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee29-136">-DefaultProfile</span></span>
<span data-ttu-id="6ee29-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee29-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ee29-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="6ee29-138">-DnsServer</span></span>
<span data-ttu-id="6ee29-139">Określa serwer DNS dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-139">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="6ee29-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="6ee29-141">Umożliwia szybsze korzystanie z sieci.</span><span class="sxs-lookup"><span data-stu-id="6ee29-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="6ee29-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="6ee29-142">-EnableIPForwarding</span></span>
<span data-ttu-id="6ee29-143">Wskazuje, że to polecenie cmdlet włącza przesyłanie dalej protokołu IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="6ee29-144">Przesyłanie dalej adresów IP umożliwia odbieranie przez maszynę wirtualną ruchu zaadresowanego do innych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6ee29-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="6ee29-145">-Force</span><span class="sxs-lookup"><span data-stu-id="6ee29-145">-Force</span></span>
<span data-ttu-id="6ee29-146">Wymusza utworzenie interfejsu sieciowego, nawet jeśli istnieje już interfejs sieciowy o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="6ee29-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="6ee29-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="6ee29-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="6ee29-148">Określa wewnętrzną etykietę nazwy DNS dla nowego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="6ee29-149">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ee29-149">-IpConfiguration</span></span>
<span data-ttu-id="6ee29-150">Określa konfigurację IP używaną przez to polecenie cmdlet dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6ee29-151">-IpConfigurationName</span></span>
<span data-ttu-id="6ee29-152">Określa nazwę konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="6ee29-152">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6ee29-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="6ee29-154">Określa obiekt **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="6ee29-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="6ee29-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6ee29-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="6ee29-156">Określa identyfikator obiektu **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="6ee29-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="6ee29-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="6ee29-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="6ee29-158">Określa konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="6ee29-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="6ee29-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="6ee29-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="6ee29-160">Określa identyfikator konfiguracji reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="6ee29-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="6ee29-161">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6ee29-161">-Location</span></span>
<span data-ttu-id="6ee29-162">Określa region dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="6ee29-163">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ee29-163">-Name</span></span>
<span data-ttu-id="6ee29-164">Określa nazwę interfejsu sieciowego, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="6ee29-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="6ee29-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6ee29-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="6ee29-166">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="6ee29-166">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6ee29-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="6ee29-168">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="6ee29-168">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="6ee29-169">-PrivateIpAddress</span></span>
<span data-ttu-id="6ee29-170">Określa statyczny adres IP IPv4, który ma zostać przypisany do tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6ee29-171">-PublicIpAddress</span></span>
<span data-ttu-id="6ee29-172">Określa obiekt **PublicIPAddress** , który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="6ee29-173">-PublicIpAddressId</span></span>
<span data-ttu-id="6ee29-174">Określa identyfikator obiektu **PublicIPAddress** , który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="6ee29-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee29-175">-ResourceGroupName</span></span>
<span data-ttu-id="6ee29-176">Określa nazwę grupy zasobów, do której należy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="6ee29-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="6ee29-177">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="6ee29-177">-Subnet</span></span>
<span data-ttu-id="6ee29-178">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="6ee29-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="6ee29-179">To polecenie cmdlet tworzy interfejs sieciowy dla podsieci, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6ee29-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6ee29-180">-SubnetId</span></span>
<span data-ttu-id="6ee29-181">Określa identyfikator podsieci, dla której ma zostać utworzony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="6ee29-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee29-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ee29-182">-Tag</span></span>
<span data-ttu-id="6ee29-183">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6ee29-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ee29-184">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="6ee29-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6ee29-185">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ee29-185">-Confirm</span></span>
<span data-ttu-id="6ee29-186">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ee29-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ee29-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ee29-187">-WhatIf</span></span>
<span data-ttu-id="6ee29-188">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ee29-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ee29-189">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ee29-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ee29-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee29-190">CommonParameters</span></span>
<span data-ttu-id="6ee29-191">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee29-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee29-192">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee29-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee29-193">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ee29-193">INPUTS</span></span>

### <span data-ttu-id="6ee29-194">System. String</span><span class="sxs-lookup"><span data-stu-id="6ee29-194">System.String</span></span>

### <span data-ttu-id="6ee29-195">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6ee29-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="6ee29-196">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="6ee29-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="6ee29-197">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6ee29-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="6ee29-198">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6ee29-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="6ee29-199">System. String []</span><span class="sxs-lookup"><span data-stu-id="6ee29-199">System.String[]</span></span>

### <span data-ttu-id="6ee29-200">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="6ee29-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="6ee29-201">Microsoft. Azure. Commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="6ee29-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="6ee29-202">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="6ee29-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="6ee29-203">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="6ee29-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="6ee29-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ee29-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6ee29-205">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ee29-205">OUTPUTS</span></span>

### <span data-ttu-id="6ee29-206">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ee29-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6ee29-207">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ee29-207">NOTES</span></span>

## <span data-ttu-id="6ee29-208">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ee29-208">RELATED LINKS</span></span>

[<span data-ttu-id="6ee29-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ee29-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="6ee29-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ee29-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="6ee29-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ee29-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)

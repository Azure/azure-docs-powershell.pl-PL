---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051102"
---
# <span data-ttu-id="bdc5f-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdc5f-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="bdc5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc5f-103">Tworzy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-103">Creates a network interface.</span></span>

## <span data-ttu-id="bdc5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdc5f-104">SYNTAX</span></span>

### <span data-ttu-id="bdc5f-105">SetByIpConfigurationResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bdc5f-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc5f-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc5f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc5f-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bdc5f-108">SetByResource</span></span>
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

## <span data-ttu-id="bdc5f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bdc5f-109">DESCRIPTION</span></span>
<span data-ttu-id="bdc5f-110">Polecenie cmdlet **New-AzNetworkInterface** tworzy interfejs sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="bdc5f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdc5f-111">EXAMPLES</span></span>

### <span data-ttu-id="bdc5f-112">Przykład 1. Tworzenie interfejsu sieciowego platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bdc5f-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="bdc5f-113">To polecenie tworzy interfejs sieciowy o nazwie NetworkInterface001 z dynamicznie przydzielonym prywatnym adresem IP z Subnet1 w sieci wirtualnej o nazwie VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="bdc5f-114">Polecenie powoduje również przypisanie dwóch serwerów DNS do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="bdc5f-115">Podrzędny zasób elementu IPConfiguration zostanie utworzony automatycznie przy użyciu nazwy IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="bdc5f-116">Przykład 2: Tworzenie interfejsu sieciowego platformy Azure przy użyciu obiektu konfiguracji IP</span><span class="sxs-lookup"><span data-stu-id="bdc5f-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="bdc5f-117">W tym przykładzie przedstawiono tworzenie nowego interfejsu sieciowego za pomocą obiektu konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="bdc5f-118">Obiekt konfiguracji IP określa statyczny prywatny adres IPv4.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="bdc5f-119">Pierwsze polecenie pobiera istniejącą określoną sieć wirtualną, która jest używana do przypisania podsieci w drugim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="bdc5f-120">Drugie polecenie tworzy konfigurację adresu IP interfejsu sieciowego o nazwie IPConfig1 i zapisuje konfigurację w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="bdc5f-121">Trzecia komenda tworzy interfejs sieciowy o nazwie NetworkInterface1, w którym jest używana konfiguracja IP interfejsu sieciowego przechowywana w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="bdc5f-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdc5f-122">PARAMETERS</span></span>

### <span data-ttu-id="bdc5f-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bdc5f-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="bdc5f-124">Określa obiekt **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="bdc5f-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="bdc5f-125">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="bdc5f-126">Określa identyfikator obiektu **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="bdc5f-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="bdc5f-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bdc5f-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="bdc5f-128">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których powinna należeć Konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="bdc5f-129">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="bdc5f-130">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których powinna należeć Konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="bdc5f-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdc5f-131">-AsJob</span></span>
<span data-ttu-id="bdc5f-132">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bdc5f-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdc5f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc5f-133">-DefaultProfile</span></span>
<span data-ttu-id="bdc5f-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc5f-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="bdc5f-135">-DnsServer</span></span>
<span data-ttu-id="bdc5f-136">Określa serwer DNS dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-136">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="bdc5f-137">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="bdc5f-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="bdc5f-138">Umożliwia szybsze korzystanie z sieci.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="bdc5f-139">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="bdc5f-139">-EnableIPForwarding</span></span>
<span data-ttu-id="bdc5f-140">Wskazuje, że to polecenie cmdlet włącza przesyłanie dalej protokołu IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="bdc5f-141">Przesyłanie dalej adresów IP umożliwia odbieranie przez maszynę wirtualną ruchu zaadresowanego do innych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="bdc5f-142">-Force</span><span class="sxs-lookup"><span data-stu-id="bdc5f-142">-Force</span></span>
<span data-ttu-id="bdc5f-143">Wymusza utworzenie interfejsu sieciowego, nawet jeśli istnieje już interfejs sieciowy o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="bdc5f-144">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="bdc5f-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="bdc5f-145">Określa wewnętrzną etykietę nazwy DNS dla nowego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-145">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="bdc5f-146">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdc5f-146">-IpConfiguration</span></span>
<span data-ttu-id="bdc5f-147">Określa konfigurację IP używaną przez to polecenie cmdlet dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="bdc5f-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bdc5f-148">-IpConfigurationName</span></span>
<span data-ttu-id="bdc5f-149">Określa nazwę konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-149">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="bdc5f-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bdc5f-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="bdc5f-151">Określa obiekt **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="bdc5f-151">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="bdc5f-152">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="bdc5f-153">Określa identyfikator obiektu **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="bdc5f-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="bdc5f-154">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="bdc5f-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="bdc5f-155">Określa konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="bdc5f-156">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="bdc5f-157">Określa identyfikator konfiguracji reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="bdc5f-158">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bdc5f-158">-Location</span></span>
<span data-ttu-id="bdc5f-159">Określa region dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-159">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="bdc5f-160">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdc5f-160">-Name</span></span>
<span data-ttu-id="bdc5f-161">Określa nazwę interfejsu sieciowego, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-161">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="bdc5f-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bdc5f-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="bdc5f-163">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="bdc5f-163">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="bdc5f-164">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="bdc5f-165">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-165">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="bdc5f-166">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdc5f-166">-PrivateIpAddress</span></span>
<span data-ttu-id="bdc5f-167">Określa statyczny adres IP IPv4, który ma zostać przypisany do tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="bdc5f-168">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdc5f-168">-PublicIpAddress</span></span>
<span data-ttu-id="bdc5f-169">Określa obiekt **PublicIPAddress** , który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="bdc5f-170">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-170">-PublicIpAddressId</span></span>
<span data-ttu-id="bdc5f-171">Określa identyfikator obiektu **PublicIPAddress** , który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="bdc5f-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc5f-172">-ResourceGroupName</span></span>
<span data-ttu-id="bdc5f-173">Określa nazwę grupy zasobów, do której należy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="bdc5f-174">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="bdc5f-174">-Subnet</span></span>
<span data-ttu-id="bdc5f-175">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="bdc5f-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="bdc5f-176">To polecenie cmdlet tworzy interfejs sieciowy dla podsieci, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdc5f-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bdc5f-177">-SubnetId</span></span>
<span data-ttu-id="bdc5f-178">Określa identyfikator podsieci, dla której ma zostać utworzony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="bdc5f-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="bdc5f-179">-Tag</span></span>
<span data-ttu-id="bdc5f-180">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bdc5f-181">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="bdc5f-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bdc5f-182">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdc5f-182">-Confirm</span></span>
<span data-ttu-id="bdc5f-183">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc5f-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc5f-184">-WhatIf</span></span>
<span data-ttu-id="bdc5f-185">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc5f-186">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc5f-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc5f-187">CommonParameters</span></span>
<span data-ttu-id="bdc5f-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc5f-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc5f-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc5f-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc5f-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdc5f-190">INPUTS</span></span>

### <span data-ttu-id="bdc5f-191">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc5f-191">System.String</span></span>

### <span data-ttu-id="bdc5f-192">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="bdc5f-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="bdc5f-193">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="bdc5f-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="bdc5f-194">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdc5f-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="bdc5f-195">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bdc5f-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="bdc5f-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="bdc5f-196">System.String[]</span></span>

### <span data-ttu-id="bdc5f-197">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="bdc5f-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="bdc5f-198">Microsoft. Azure. Commands. Network. models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="bdc5f-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="bdc5f-199">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="bdc5f-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="bdc5f-200">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="bdc5f-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="bdc5f-201">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bdc5f-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bdc5f-202">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdc5f-202">OUTPUTS</span></span>

### <span data-ttu-id="bdc5f-203">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdc5f-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="bdc5f-204">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdc5f-204">NOTES</span></span>

## <span data-ttu-id="bdc5f-205">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdc5f-205">RELATED LINKS</span></span>

[<span data-ttu-id="bdc5f-206">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdc5f-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="bdc5f-207">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdc5f-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="bdc5f-208">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdc5f-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)

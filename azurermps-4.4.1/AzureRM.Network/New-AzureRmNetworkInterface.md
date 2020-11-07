---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 75e16da63a5348b47a5b67042a2fb1e2078206c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718153"
---
# <span data-ttu-id="b5073-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5073-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="b5073-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5073-102">SYNOPSIS</span></span>
<span data-ttu-id="b5073-103">Tworzy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="b5073-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5073-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5073-104">SYNTAX</span></span>

### <span data-ttu-id="b5073-105">SetByIpConfigurationResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5073-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5073-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b5073-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5073-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5073-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5073-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b5073-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5073-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b5073-109">DESCRIPTION</span></span>
<span data-ttu-id="b5073-110">Polecenie cmdlet **New-AzureRmNetworkInterface** tworzy interfejs sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="b5073-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="b5073-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5073-111">EXAMPLES</span></span>

### <span data-ttu-id="b5073-112">Przykład 1. Tworzenie interfejsu sieciowego platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b5073-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="b5073-113">To polecenie tworzy interfejs sieciowy o nazwie NetworkInterface001 z dynamicznie przydzielonym prywatnym adresem IP z Subnet1 w sieci wirtualnej o nazwie VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="b5073-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="b5073-114">Polecenie powoduje również przypisanie dwóch serwerów DNS do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="b5073-115">Podrzędny zasób elementu IPConfiguration zostanie utworzony automatycznie przy użyciu nazwy IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="b5073-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="b5073-116">Przykład 2: Tworzenie interfejsu sieciowego platformy Azure przy użyciu obiektu konfiguracji IP</span><span class="sxs-lookup"><span data-stu-id="b5073-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="b5073-117">W tym przykładzie przedstawiono tworzenie nowego interfejsu sieciowego za pomocą obiektu konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="b5073-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="b5073-118">Obiekt konfiguracji IP określa statyczny prywatny adres IPv4.</span><span class="sxs-lookup"><span data-stu-id="b5073-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="b5073-119">Pierwsze polecenie powoduje utworzenie konfiguracji adresu IP interfejsu sieciowego o nazwie IPConfig1 i zapisanie konfiguracji w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="b5073-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="b5073-120">Drugie polecenie tworzy interfejs sieciowy o nazwie NetworkInterface1, w którym jest używana konfiguracja IP interfejsu sieciowego przechowywana w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="b5073-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="b5073-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5073-121">PARAMETERS</span></span>

### <span data-ttu-id="b5073-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b5073-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="b5073-123">Określa obiekt **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="b5073-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="b5073-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b5073-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="b5073-125">Określa identyfikator obiektu **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="b5073-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="b5073-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5073-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="b5073-127">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których powinna należeć Konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="b5073-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b5073-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="b5073-129">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których powinna należeć Konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="b5073-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5073-130">-DefaultProfile</span></span>
<span data-ttu-id="b5073-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5073-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5073-132">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="b5073-132">-DnsServer</span></span>
<span data-ttu-id="b5073-133">Określa serwer DNS dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-133">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5073-134">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="b5073-134">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="b5073-135">Umożliwia szybsze korzystanie z sieci.</span><span class="sxs-lookup"><span data-stu-id="b5073-135">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="b5073-136">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="b5073-136">-EnableIPForwarding</span></span>
<span data-ttu-id="b5073-137">Wskazuje, że to polecenie cmdlet włącza przesyłanie dalej protokołu IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-137">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="b5073-138">Przesyłanie dalej adresów IP umożliwia odbieranie przez maszynę wirtualną ruchu zaadresowanego do innych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b5073-138">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="b5073-139">-Force</span><span class="sxs-lookup"><span data-stu-id="b5073-139">-Force</span></span>
<span data-ttu-id="b5073-140">Wymusza utworzenie interfejsu sieciowego, nawet jeśli istnieje już interfejs sieciowy o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="b5073-140">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="b5073-141">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="b5073-141">-InternalDnsNameLabel</span></span>
<span data-ttu-id="b5073-142">Określa wewnętrzną etykietę nazwy DNS dla nowego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-142">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="b5073-143">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5073-143">-IpConfiguration</span></span>
<span data-ttu-id="b5073-144">Określa konfigurację IP używaną przez to polecenie cmdlet dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-144">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5073-145">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b5073-145">-IpConfigurationName</span></span>
<span data-ttu-id="b5073-146">Określa nazwę konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="b5073-146">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="b5073-147">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b5073-147">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="b5073-148">Określa obiekt **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="b5073-148">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="b5073-149">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b5073-149">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="b5073-150">Określa identyfikator obiektu **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="b5073-150">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="b5073-151">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="b5073-151">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="b5073-152">Określa konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b5073-152">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="b5073-153">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="b5073-153">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="b5073-154">Określa identyfikator konfiguracji reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b5073-154">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="b5073-155">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b5073-155">-Location</span></span>
<span data-ttu-id="b5073-156">Określa region dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-156">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="b5073-157">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5073-157">-Name</span></span>
<span data-ttu-id="b5073-158">Określa nazwę interfejsu sieciowego, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="b5073-158">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="b5073-159">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5073-159">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b5073-160">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="b5073-160">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="b5073-161">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b5073-161">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b5073-162">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b5073-162">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="b5073-163">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5073-163">-PrivateIpAddress</span></span>
<span data-ttu-id="b5073-164">Określa statyczny adres IP IPv4, który ma zostać przypisany do tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-164">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="b5073-165">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5073-165">-PublicIpAddress</span></span>
<span data-ttu-id="b5073-166">Określa obiekt **PublicIPAddress** , który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-166">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="b5073-167">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b5073-167">-PublicIpAddressId</span></span>
<span data-ttu-id="b5073-168">Określa identyfikator obiektu **PublicIPAddress** , który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="b5073-168">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="b5073-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5073-169">-ResourceGroupName</span></span>
<span data-ttu-id="b5073-170">Określa nazwę grupy zasobów, do której należy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="b5073-170">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="b5073-171">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="b5073-171">-Subnet</span></span>
<span data-ttu-id="b5073-172">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="b5073-172">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="b5073-173">To polecenie cmdlet tworzy interfejs sieciowy dla podsieci, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b5073-173">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5073-174">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b5073-174">-SubnetId</span></span>
<span data-ttu-id="b5073-175">Określa identyfikator podsieci, dla której ma zostać utworzony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="b5073-175">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="b5073-176">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5073-176">-Tag</span></span>
<span data-ttu-id="b5073-177">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b5073-177">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b5073-178">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="b5073-178">For example:</span></span>

<span data-ttu-id="b5073-179">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="b5073-179">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b5073-180">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5073-180">-Confirm</span></span>
<span data-ttu-id="b5073-181">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5073-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5073-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5073-182">-WhatIf</span></span>
<span data-ttu-id="b5073-183">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5073-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5073-184">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5073-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5073-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5073-185">CommonParameters</span></span>
<span data-ttu-id="b5073-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5073-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5073-187">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5073-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5073-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5073-188">INPUTS</span></span>

## <span data-ttu-id="b5073-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5073-189">OUTPUTS</span></span>

### <span data-ttu-id="b5073-190">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5073-190">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b5073-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5073-191">NOTES</span></span>

## <span data-ttu-id="b5073-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5073-192">RELATED LINKS</span></span>

[<span data-ttu-id="b5073-193">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5073-193">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="b5073-194">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5073-194">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="b5073-195">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b5073-195">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)

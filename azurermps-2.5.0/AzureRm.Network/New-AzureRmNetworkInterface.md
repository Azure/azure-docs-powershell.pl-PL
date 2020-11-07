---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 1a87b7bfa4c497ad7d09a9e84d972d548e2031b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898722"
---
# <span data-ttu-id="a9b54-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a9b54-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="a9b54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9b54-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b54-103">Tworzy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="a9b54-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9b54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9b54-104">SYNTAX</span></span>

### <span data-ttu-id="a9b54-105">SetByIpConfigurationResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9b54-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9b54-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b54-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9b54-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b54-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9b54-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a9b54-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9b54-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a9b54-109">DESCRIPTION</span></span>
<span data-ttu-id="a9b54-110">Polecenie cmdlet **New-AzureRmNetworkInterface** tworzy interfejs sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b54-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="a9b54-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9b54-111">EXAMPLES</span></span>

### <span data-ttu-id="a9b54-112">Przykład 1. Tworzenie interfejsu sieciowego platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a9b54-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="a9b54-113">To polecenie tworzy interfejs sieciowy o nazwie NetworkInterface001 z dynamicznie przydzielonym prywatnym adresem IP z Subnet1 w sieci wirtualnej o nazwie VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="a9b54-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="a9b54-114">Polecenie powoduje również przypisanie dwóch serwerów DNS do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="a9b54-115">Podrzędny zasób elementu IPConfiguration zostanie utworzony automatycznie przy użyciu nazwy IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="a9b54-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="a9b54-116">Przykład 2: Tworzenie interfejsu sieciowego platformy Azure przy użyciu obiektu konfiguracji IP</span><span class="sxs-lookup"><span data-stu-id="a9b54-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="a9b54-117">W tym przykładzie przedstawiono tworzenie nowego interfejsu sieciowego za pomocą obiektu konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="a9b54-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="a9b54-118">Obiekt konfiguracji IP określa statyczny prywatny adres IPv4.</span><span class="sxs-lookup"><span data-stu-id="a9b54-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="a9b54-119">Pierwsze polecenie powoduje utworzenie konfiguracji adresu IP interfejsu sieciowego o nazwie IPConfig1 i zapisanie konfiguracji w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="a9b54-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="a9b54-120">Drugie polecenie tworzy interfejs sieciowy o nazwie NetworkInterface1, w którym jest używana konfiguracja IP interfejsu sieciowego przechowywana w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="a9b54-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="a9b54-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9b54-121">PARAMETERS</span></span>

### <span data-ttu-id="a9b54-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9b54-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="a9b54-123">Określa obiekt **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="a9b54-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a9b54-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a9b54-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="a9b54-125">Określa identyfikator obiektu **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="a9b54-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a9b54-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a9b54-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="a9b54-127">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których powinna należeć Konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="a9b54-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a9b54-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="a9b54-129">Określa kolekcję odwołań do grup zabezpieczeń aplikacji, do których powinna należeć Konfiguracja IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="a9b54-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9b54-130">-AsJob</span></span>
<span data-ttu-id="a9b54-131">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a9b54-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9b54-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b54-132">-DefaultProfile</span></span>
<span data-ttu-id="a9b54-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b54-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9b54-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="a9b54-134">-DnsServer</span></span>
<span data-ttu-id="a9b54-135">Określa serwer DNS dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="a9b54-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="a9b54-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="a9b54-137">Umożliwia szybsze korzystanie z sieci.</span><span class="sxs-lookup"><span data-stu-id="a9b54-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="a9b54-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a9b54-138">-EnableIPForwarding</span></span>
<span data-ttu-id="a9b54-139">Wskazuje, że to polecenie cmdlet włącza przesyłanie dalej protokołu IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="a9b54-140">Przesyłanie dalej adresów IP umożliwia odbieranie przez maszynę wirtualną ruchu zaadresowanego do innych lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9b54-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="a9b54-141">-Force</span><span class="sxs-lookup"><span data-stu-id="a9b54-141">-Force</span></span>
<span data-ttu-id="a9b54-142">Wymusza utworzenie interfejsu sieciowego, nawet jeśli istnieje już interfejs sieciowy o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="a9b54-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="a9b54-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="a9b54-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="a9b54-144">Określa wewnętrzną etykietę nazwy DNS dla nowego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-145">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9b54-145">-IpConfiguration</span></span>
<span data-ttu-id="a9b54-146">Określa konfigurację IP używaną przez to polecenie cmdlet dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="a9b54-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a9b54-147">-IpConfigurationName</span></span>
<span data-ttu-id="a9b54-148">Określa nazwę konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="a9b54-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9b54-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="a9b54-150">Określa obiekt **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="a9b54-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a9b54-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a9b54-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="a9b54-152">Określa identyfikator obiektu **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="a9b54-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a9b54-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a9b54-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="a9b54-154">Określa konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a9b54-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="a9b54-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="a9b54-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="a9b54-156">Określa identyfikator konfiguracji reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a9b54-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="a9b54-157">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a9b54-157">-Location</span></span>
<span data-ttu-id="a9b54-158">Określa region dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9b54-159">-Name</span></span>
<span data-ttu-id="a9b54-160">Określa nazwę interfejsu sieciowego, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="a9b54-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a9b54-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a9b54-162">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="a9b54-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a9b54-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a9b54-164">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="a9b54-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9b54-165">-PrivateIpAddress</span></span>
<span data-ttu-id="a9b54-166">Określa statyczny adres IP IPv4, który ma zostać przypisany do tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9b54-167">-PublicIpAddress</span></span>
<span data-ttu-id="a9b54-168">Określa obiekt **PublicIPAddress** , który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a9b54-169">-PublicIpAddressId</span></span>
<span data-ttu-id="a9b54-170">Określa identyfikator obiektu **PublicIPAddress** , który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a9b54-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b54-171">-ResourceGroupName</span></span>
<span data-ttu-id="a9b54-172">Określa nazwę grupy zasobów, do której należy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="a9b54-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-173">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="a9b54-173">-Subnet</span></span>
<span data-ttu-id="a9b54-174">Określa obiekt **podsieci** .</span><span class="sxs-lookup"><span data-stu-id="a9b54-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="a9b54-175">To polecenie cmdlet tworzy interfejs sieciowy dla podsieci, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a9b54-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a9b54-176">-SubnetId</span></span>
<span data-ttu-id="a9b54-177">Określa identyfikator podsieci, dla której ma zostać utworzony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="a9b54-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9b54-178">-Tag</span></span>
<span data-ttu-id="a9b54-179">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a9b54-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a9b54-180">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a9b54-180">For example:</span></span>

<span data-ttu-id="a9b54-181">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a9b54-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-182">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9b54-182">-Confirm</span></span>
<span data-ttu-id="a9b54-183">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b54-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9b54-184">-WhatIf</span></span>
<span data-ttu-id="a9b54-185">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b54-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9b54-186">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9b54-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b54-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b54-187">CommonParameters</span></span>
<span data-ttu-id="a9b54-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b54-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b54-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9b54-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b54-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9b54-190">INPUTS</span></span>

## <span data-ttu-id="a9b54-191">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9b54-191">OUTPUTS</span></span>

### <span data-ttu-id="a9b54-192">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a9b54-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a9b54-193">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9b54-193">NOTES</span></span>

## <span data-ttu-id="a9b54-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9b54-194">RELATED LINKS</span></span>

[<span data-ttu-id="a9b54-195">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a9b54-195">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="a9b54-196">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a9b54-196">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="a9b54-197">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a9b54-197">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)

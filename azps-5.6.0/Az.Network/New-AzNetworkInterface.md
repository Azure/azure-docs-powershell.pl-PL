---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 994c0e85745e08d4a01e7b5a20b90a25513a983f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984425"
---
# <span data-ttu-id="4364f-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4364f-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="4364f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4364f-102">SYNOPSIS</span></span>
<span data-ttu-id="4364f-103">Tworzy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="4364f-103">Creates a network interface.</span></span>

## <span data-ttu-id="4364f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4364f-104">SYNTAX</span></span>

### <span data-ttu-id="4364f-105">SetByIpConfigurationResource (Default)</span><span class="sxs-lookup"><span data-stu-id="4364f-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4364f-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="4364f-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4364f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4364f-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4364f-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4364f-108">SetByResource</span></span>
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

## <span data-ttu-id="4364f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="4364f-109">DESCRIPTION</span></span>
<span data-ttu-id="4364f-110">Polecenie **cmdlet New-AzNetworkInterface** tworzy interfejs sieciowy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4364f-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="4364f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4364f-111">EXAMPLES</span></span>

### <span data-ttu-id="4364f-112">Przykład 1. Tworzenie interfejsu sieciowego platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4364f-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="4364f-113">To polecenie tworzy interfejs sieciowy o nazwie NetworkInterface001 z dynamicznie przypisanym prywatnym adresem IP z podsieci1 w sieci wirtualnej o nazwie VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="4364f-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="4364f-114">To polecenie przypisuje również do interfejsu sieciowego dwa serwery DNS.</span><span class="sxs-lookup"><span data-stu-id="4364f-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="4364f-115">Zasób podrzędny IPConfiguration zostanie utworzony automatycznie przy użyciu nazwy IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="4364f-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="4364f-116">Przykład 2. Tworzenie interfejsu sieciowego platformy Azure przy użyciu obiektu konfiguracji adresu IP</span><span class="sxs-lookup"><span data-stu-id="4364f-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="4364f-117">W tym przykładzie jest tworzenie nowego interfejsu sieciowego przy użyciu obiektu konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="4364f-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="4364f-118">Obiekt konfiguracji adresu IP określa statyczny prywatny adres IPv4.</span><span class="sxs-lookup"><span data-stu-id="4364f-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="4364f-119">Pierwsze polecenie pobiera istniejącą określoną sieć wirtualną używaną do przypisania podsieci w drugim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="4364f-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="4364f-120">Drugie polecenie tworzy konfigurację protokołu IP interfejsu sieciowego o nazwie IPConfig1 i zapisuje konfigurację w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="4364f-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="4364f-121">Trzecie polecenie tworzy interfejs sieciowy o nazwie NetworkInterface1, który używa konfiguracji protokołu IP interfejsu sieciowego przechowywanej w zmiennej o nazwie $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="4364f-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="4364f-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4364f-122">Example 3</span></span>

<span data-ttu-id="4364f-123">Tworzy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="4364f-123">Creates a network interface.</span></span> <span data-ttu-id="4364f-124">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="4364f-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="4364f-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4364f-125">PARAMETERS</span></span>

### <span data-ttu-id="4364f-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4364f-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="4364f-127">Określa obiekt **ApplicationGatewayBackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="4364f-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="4364f-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4364f-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="4364f-129">Określa identyfikator obiektu **ApplicationGatewayBackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="4364f-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="4364f-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4364f-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="4364f-131">Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których powinna należeć konfiguracja protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="4364f-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4364f-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="4364f-133">Określa zbiór odwołań do grup zabezpieczeń aplikacji, do których powinna należeć konfiguracja protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="4364f-134">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4364f-134">-AsJob</span></span>
<span data-ttu-id="4364f-135">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4364f-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4364f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4364f-136">-DefaultProfile</span></span>
<span data-ttu-id="4364f-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4364f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4364f-138">- DnsServer</span><span class="sxs-lookup"><span data-stu-id="4364f-138">-DnsServer</span></span>
<span data-ttu-id="4364f-139">Określa serwer DNS dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="4364f-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="4364f-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="4364f-141">Włącza tryb przyspieszony sieci.</span><span class="sxs-lookup"><span data-stu-id="4364f-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="4364f-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="4364f-142">-EnableIPForwarding</span></span>
<span data-ttu-id="4364f-143">Wskazuje, że to polecenie cmdlet umożliwia przesyłanie dalej adresów IP dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="4364f-144">Przekazywanie adresów IP umożliwia maszynie wirtualnej odbieranie ruchu zaadresowanych do innych miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="4364f-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="4364f-145">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="4364f-145">-Force</span></span>
<span data-ttu-id="4364f-146">Wymusza utworzenie interfejsu sieciowego, nawet jeśli interfejs sieciowy o tej samej nazwie już istnieje.</span><span class="sxs-lookup"><span data-stu-id="4364f-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="4364f-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="4364f-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="4364f-148">Określa wewnętrzną etykietę nazwy DNS dla nowego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="4364f-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4364f-149">-IpConfiguration</span></span>
<span data-ttu-id="4364f-150">Określa konfigurację protokołu IP używaną przez to polecenie cmdlet dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="4364f-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4364f-151">-IpConfigurationName</span></span>
<span data-ttu-id="4364f-152">Określa nazwę konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="4364f-152">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="4364f-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4364f-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="4364f-154">Określa obiekt **BackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="4364f-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="4364f-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4364f-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="4364f-156">Określa identyfikator obiektu **BackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="4364f-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="4364f-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="4364f-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="4364f-158">Określa konfigurację reguły nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4364f-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="4364f-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="4364f-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="4364f-160">Określa identyfikator konfiguracji reguły nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4364f-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="4364f-161">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4364f-161">-Location</span></span>
<span data-ttu-id="4364f-162">Określa region interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="4364f-163">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4364f-163">-Name</span></span>
<span data-ttu-id="4364f-164">Określa nazwę interfejsu sieciowego do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4364f-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="4364f-165">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4364f-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4364f-166">Określa obiekt **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="4364f-166">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="4364f-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4364f-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="4364f-168">Określa identyfikator sieciowej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="4364f-168">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="4364f-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4364f-169">-PrivateIpAddress</span></span>
<span data-ttu-id="4364f-170">Określa statyczny adres IP IPv4, który należy przypisać do tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="4364f-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4364f-171">-PublicIpAddress</span></span>
<span data-ttu-id="4364f-172">Określa obiekt **PublicIPAddress,** który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="4364f-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4364f-173">-PublicIpAddressId</span></span>
<span data-ttu-id="4364f-174">Określa identyfikator obiektu **PublicIPAddress,** który ma zostać przypisany do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="4364f-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="4364f-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4364f-175">-ResourceGroupName</span></span>
<span data-ttu-id="4364f-176">Określa nazwę grupy zasobów, do której należy interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="4364f-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="4364f-177">-Subnet</span><span class="sxs-lookup"><span data-stu-id="4364f-177">-Subnet</span></span>
<span data-ttu-id="4364f-178">Określa obiekt **Podsieci.**</span><span class="sxs-lookup"><span data-stu-id="4364f-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="4364f-179">To polecenie cmdlet tworzy interfejs sieciowy dla podsieci, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4364f-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="4364f-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4364f-180">-SubnetId</span></span>
<span data-ttu-id="4364f-181">Określa identyfikator podsieci, dla której ma być tworzyć interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="4364f-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="4364f-182">— Tag</span><span class="sxs-lookup"><span data-stu-id="4364f-182">-Tag</span></span>
<span data-ttu-id="4364f-183">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="4364f-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4364f-184">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4364f-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4364f-185">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4364f-185">-Confirm</span></span>
<span data-ttu-id="4364f-186">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4364f-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4364f-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4364f-187">-WhatIf</span></span>
<span data-ttu-id="4364f-188">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4364f-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4364f-189">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4364f-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4364f-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4364f-190">CommonParameters</span></span>
<span data-ttu-id="4364f-191">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4364f-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4364f-192">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4364f-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4364f-193">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4364f-193">INPUTS</span></span>

### <span data-ttu-id="4364f-194">System.String</span><span class="sxs-lookup"><span data-stu-id="4364f-194">System.String</span></span>

### <span data-ttu-id="4364f-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="4364f-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="4364f-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4364f-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="4364f-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4364f-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="4364f-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4364f-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="4364f-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4364f-199">System.String[]</span></span>

### <span data-ttu-id="4364f-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="4364f-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="4364f-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="4364f-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="4364f-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="4364f-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="4364f-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="4364f-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="4364f-204">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4364f-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4364f-205">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4364f-205">OUTPUTS</span></span>

### <span data-ttu-id="4364f-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4364f-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4364f-207">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4364f-207">NOTES</span></span>

## <span data-ttu-id="4364f-208">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4364f-208">RELATED LINKS</span></span>

[<span data-ttu-id="4364f-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4364f-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="4364f-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4364f-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="4364f-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4364f-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)

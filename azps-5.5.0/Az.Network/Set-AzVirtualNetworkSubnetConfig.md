---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fe6c67c39ef3d14ec1b1e4200b4fad09aa7d2a24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191586"
---
# <span data-ttu-id="19124-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19124-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="19124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19124-102">SYNOPSIS</span></span>
<span data-ttu-id="19124-103">Aktualizuje konfigurację podsieci dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19124-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="19124-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="19124-104">SYNTAX</span></span>

### <span data-ttu-id="19124-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="19124-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19124-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="19124-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19124-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="19124-107">DESCRIPTION</span></span>
<span data-ttu-id="19124-108">Polecenie **cmdlet Set-AzVirtualNetworkSubnetConfig** aktualizuje konfigurację podsieci dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19124-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="19124-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="19124-109">EXAMPLES</span></span>

### <span data-ttu-id="19124-110">1. Modyfikowanie prefiksu adresu podsieci</span><span class="sxs-lookup"><span data-stu-id="19124-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="19124-111">W tym przykładzie jest tworzyna sieć wirtualna z jedną podsiecią.</span><span class="sxs-lookup"><span data-stu-id="19124-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="19124-112">Następnie jest Set-AzVirtualNetworkSubnetConfig w celu zmodyfikowania poprawki AddressPrefix podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="19124-113">Ma to wpływ tylko na reprezentację w pamięci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19124-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="19124-114">Set-AzVirtualNetwork jest wywoływana w celu modyfikowania sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="19124-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="19124-115">2. Dodawanie grupy zabezpieczeń sieciowych do podsieci</span><span class="sxs-lookup"><span data-stu-id="19124-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="19124-116">W tym przykładzie jest grupę zasobów zawierającą jedną sieć wirtualną zawierającą tylko jedną podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="19124-117">Następnie tworzy grupę zabezpieczeń sieciowych z regułą zezwalania na ruch RDP.</span><span class="sxs-lookup"><span data-stu-id="19124-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="19124-118">Polecenie Set-AzVirtualNetworkSubnetConfig cmdlet służy do modyfikowania reprezentacji w pamięci podsieci frontendowej tak, aby wskazuje nowo utworzoną grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="19124-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="19124-119">Polecenie Set-AzVirtualNetwork cmdlet jest następnie wywoływane w celu napisania zmodyfikowanego stanu z powrotem do usługi.</span><span class="sxs-lookup"><span data-stu-id="19124-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="19124-120">3. Dołączanie bramy nat do podsieci</span><span class="sxs-lookup"><span data-stu-id="19124-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="19124-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19124-121">PARAMETERS</span></span>

### <span data-ttu-id="19124-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="19124-122">-AddressPrefix</span></span>
<span data-ttu-id="19124-123">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19124-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19124-124">-DefaultProfile</span></span>
<span data-ttu-id="19124-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="19124-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19124-126">— Delegowanie</span><span class="sxs-lookup"><span data-stu-id="19124-126">-Delegation</span></span>
<span data-ttu-id="19124-127">Lista usług z uprawnieniami do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-127">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19124-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19124-128">-InputObject</span></span>
<span data-ttu-id="19124-129">Określa bramę nat skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19124-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="19124-130">-IpAllocation</span></span>
<span data-ttu-id="19124-131">Określa alokacje IpAllocations dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-131">Specifies IpAllocations for a subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19124-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="19124-132">-Name</span></span>
<span data-ttu-id="19124-133">Określa nazwę konfiguracji podsieci konfigurowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19124-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="19124-134">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19124-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="19124-135">Określa obiekt **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="19124-135">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19124-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="19124-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="19124-137">Określa identyfikator sieciowej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="19124-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="19124-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="19124-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="19124-139">Konfigurowanie włączania lub wyłączania stosowania zasad sieciowych do prywatnego punktu końcowego w podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="19124-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="19124-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="19124-141">Konfigurowanie włączania lub wyłączania stosowania zasad sieciowych w prywatnej usłudze linków w podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="19124-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19124-142">-ResourceId</span></span>
<span data-ttu-id="19124-143">Określa identyfikator zasobu bramy NAT skojarzonego z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19124-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="19124-144">-RouteTable</span></span>
<span data-ttu-id="19124-145">Określa obiekt tabeli trasy skojarzony z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="19124-145">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19124-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="19124-146">-RouteTableId</span></span>
<span data-ttu-id="19124-147">Określa identyfikator obiektu tabeli trasy skojarzonego z grupą zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="19124-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="19124-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="19124-148">-ServiceEndpoint</span></span>
<span data-ttu-id="19124-149">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="19124-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="19124-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19124-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="19124-151">Zasady punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="19124-151">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19124-152">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19124-152">-VirtualNetwork</span></span>
<span data-ttu-id="19124-153">Określa obiekt **VirtualNetwork** zawierający konfigurację podsieci.</span><span class="sxs-lookup"><span data-stu-id="19124-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19124-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19124-154">CommonParameters</span></span>
<span data-ttu-id="19124-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19124-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19124-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19124-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19124-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19124-157">INPUTS</span></span>

### <span data-ttu-id="19124-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19124-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="19124-159">System.String</span><span class="sxs-lookup"><span data-stu-id="19124-159">System.String</span></span>

### <span data-ttu-id="19124-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19124-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="19124-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="19124-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="19124-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="19124-162">System.String[]</span></span>

### <span data-ttu-id="19124-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="19124-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="19124-164">Microsoft.Azure.Commands.Network.Models.PSDelegacji[]</span><span class="sxs-lookup"><span data-stu-id="19124-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="19124-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19124-165">OUTPUTS</span></span>

### <span data-ttu-id="19124-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19124-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="19124-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="19124-167">NOTES</span></span>

## <span data-ttu-id="19124-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19124-168">RELATED LINKS</span></span>

[<span data-ttu-id="19124-169">Add-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19124-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19124-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19124-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19124-171">New-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19124-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19124-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19124-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

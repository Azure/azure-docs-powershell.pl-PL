---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 47c56f2f55a07dc2567ca3ee2030e075d90dc324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952026"
---
# <span data-ttu-id="f3aaf-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f3aaf-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="f3aaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="f3aaf-103">Aktualizuje konfigurację podsieci dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="f3aaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f3aaf-104">SYNTAX</span></span>

### <span data-ttu-id="f3aaf-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f3aaf-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3aaf-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3aaf-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3aaf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f3aaf-107">DESCRIPTION</span></span>
<span data-ttu-id="f3aaf-108">Polecenie **cmdlet Set-AzVirtualNetworkSubnetConfig** aktualizuje konfigurację podsieci dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="f3aaf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f3aaf-109">EXAMPLES</span></span>

### <span data-ttu-id="f3aaf-110">1. Modyfikowanie prefiksu adresu podsieci</span><span class="sxs-lookup"><span data-stu-id="f3aaf-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="f3aaf-111">W tym przykładzie jest tworzyna sieć wirtualna z jedną podsiecią.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="f3aaf-112">Następnie wywołania Set-AzVirtualNetworkSubnetConfig modyfikowania poprawki AddressPrefix podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="f3aaf-113">Ma to wpływ tylko na reprezentację w pamięci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="f3aaf-114">Set-AzVirtualNetwork jest wywoływana w celu modyfikowania sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="f3aaf-115">2. Dodawanie grupy zabezpieczeń sieciowych do podsieci</span><span class="sxs-lookup"><span data-stu-id="f3aaf-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="f3aaf-116">W tym przykładzie jest grupę zasobów zawierającą jedną sieć wirtualną zawierającą tylko jedną podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="f3aaf-117">Następnie tworzy grupę zabezpieczeń sieciowych z regułą zezwalania na ruch RDP.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="f3aaf-118">Polecenie Set-AzVirtualNetworkSubnetConfig cmdlet służy do modyfikowania reprezentacji w pamięci podsieci frontendowej tak, aby wskazuje nowo utworzoną grupę zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="f3aaf-119">Polecenie Set-AzVirtualNetwork cmdlet jest następnie wywoływane w celu napisania zmodyfikowanego stanu z powrotem do usługi.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="f3aaf-120">3. Dołączanie bramy nat do podsieci</span><span class="sxs-lookup"><span data-stu-id="f3aaf-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="f3aaf-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3aaf-121">PARAMETERS</span></span>

### <span data-ttu-id="f3aaf-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f3aaf-122">-AddressPrefix</span></span>
<span data-ttu-id="f3aaf-123">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="f3aaf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3aaf-124">-DefaultProfile</span></span>
<span data-ttu-id="f3aaf-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3aaf-126">—Delegowanie</span><span class="sxs-lookup"><span data-stu-id="f3aaf-126">-Delegation</span></span>
<span data-ttu-id="f3aaf-127">Lista usług z uprawnieniami do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="f3aaf-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3aaf-128">-InputObject</span></span>
<span data-ttu-id="f3aaf-129">Określa bramę nat skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="f3aaf-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="f3aaf-130">-IpAllocation</span></span>
<span data-ttu-id="f3aaf-131">Określa alokacje IpAllocations dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-131">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="f3aaf-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f3aaf-132">-Name</span></span>
<span data-ttu-id="f3aaf-133">Określa nazwę konfiguracji podsieci konfigurowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="f3aaf-134">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f3aaf-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f3aaf-135">Określa obiekt **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="f3aaf-135">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="f3aaf-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f3aaf-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f3aaf-137">Określa identyfikator sieciowej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="f3aaf-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="f3aaf-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="f3aaf-139">Konfigurowanie włączania lub wyłączania stosowania zasad sieciowych do prywatnego punktu końcowego w podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="f3aaf-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="f3aaf-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="f3aaf-141">Konfigurowanie włączania lub wyłączania stosowania zasad sieciowych w prywatnej usłudze linków w podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="f3aaf-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3aaf-142">-ResourceId</span></span>
<span data-ttu-id="f3aaf-143">Określa identyfikator zasobu bramy NAT skojarzonego z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="f3aaf-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f3aaf-144">-RouteTable</span></span>
<span data-ttu-id="f3aaf-145">Określa obiekt tabeli trasy skojarzony z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-145">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="f3aaf-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="f3aaf-146">-RouteTableId</span></span>
<span data-ttu-id="f3aaf-147">Określa identyfikator obiektu tabeli trasy skojarzonego z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="f3aaf-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3aaf-148">-ServiceEndpoint</span></span>
<span data-ttu-id="f3aaf-149">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="f3aaf-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="f3aaf-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f3aaf-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f3aaf-151">Zasady punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="f3aaf-151">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="f3aaf-152">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3aaf-152">-VirtualNetwork</span></span>
<span data-ttu-id="f3aaf-153">Określa obiekt **VirtualNetwork** zawierający konfigurację podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="f3aaf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3aaf-154">CommonParameters</span></span>
<span data-ttu-id="f3aaf-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3aaf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3aaf-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3aaf-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3aaf-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3aaf-157">INPUTS</span></span>

### <span data-ttu-id="f3aaf-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3aaf-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="f3aaf-159">System.String</span><span class="sxs-lookup"><span data-stu-id="f3aaf-159">System.String</span></span>

### <span data-ttu-id="f3aaf-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f3aaf-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="f3aaf-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3aaf-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="f3aaf-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f3aaf-162">System.String[]</span></span>

### <span data-ttu-id="f3aaf-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="f3aaf-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="f3aaf-164">Microsoft.Azure.Commands.Network.Models.PSDelegacji[]</span><span class="sxs-lookup"><span data-stu-id="f3aaf-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="f3aaf-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3aaf-165">OUTPUTS</span></span>

### <span data-ttu-id="f3aaf-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3aaf-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f3aaf-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f3aaf-167">NOTES</span></span>

## <span data-ttu-id="f3aaf-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3aaf-168">RELATED LINKS</span></span>

[<span data-ttu-id="f3aaf-169">Add-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f3aaf-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f3aaf-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f3aaf-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f3aaf-171">New-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f3aaf-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f3aaf-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f3aaf-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

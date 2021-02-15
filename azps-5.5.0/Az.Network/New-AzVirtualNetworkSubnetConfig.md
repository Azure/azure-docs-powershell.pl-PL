---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202695"
---
# <span data-ttu-id="53592-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="53592-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="53592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53592-102">SYNOPSIS</span></span>
<span data-ttu-id="53592-103">Tworzy konfigurację podsieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="53592-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="53592-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53592-104">SYNTAX</span></span>

### <span data-ttu-id="53592-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="53592-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53592-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53592-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53592-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="53592-107">DESCRIPTION</span></span>
<span data-ttu-id="53592-108">**Polecenie cmdlet New-AzVirtualNetworkSubnetConfig** tworzy konfigurację podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="53592-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="53592-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53592-109">EXAMPLES</span></span>

### <span data-ttu-id="53592-110">Przykład 1. Tworzenie sieci wirtualnej z dwiema podsieciami i grupą zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="53592-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="53592-111">W tym przykładzie są tworzyć dwie nowe konfiguracje podsieci przy New-AzVirtualSubnetConfig cmdlet, a następnie używać ich do tworzenia sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="53592-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="53592-112">Szablon New-AzVirtualSubnetConfig tworzy jedynie reprezentację podsieci w pamięci.</span><span class="sxs-lookup"><span data-stu-id="53592-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="53592-113">W tym przykładzie frontendSubnet ma kod CIDR 10.0.1.0/24 i odwołuje się do grupy zabezpieczeń sieci, która zezwala na dostęp za ich względów.</span><span class="sxs-lookup"><span data-stu-id="53592-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="53592-114">W przypadku podsieci wewnętrznej ma kod CIDR 10.0.2.0/24 i odwołuje się do tej samej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="53592-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="53592-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53592-115">PARAMETERS</span></span>

### <span data-ttu-id="53592-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="53592-116">-AddressPrefix</span></span>
<span data-ttu-id="53592-117">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="53592-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53592-118">-DefaultProfile</span></span>
<span data-ttu-id="53592-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="53592-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53592-120">—Delegowanie</span><span class="sxs-lookup"><span data-stu-id="53592-120">-Delegation</span></span>
<span data-ttu-id="53592-121">Lista usług z uprawnieniami do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="53592-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53592-122">-InputObject</span></span>
<span data-ttu-id="53592-123">Określa bramę nat skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="53592-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="53592-124">-IpAllocation</span></span>
<span data-ttu-id="53592-125">Określa alokacje IpAllocations dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="53592-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="53592-126">-Name</span></span>
<span data-ttu-id="53592-127">Określa nazwę konfiguracji podsieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="53592-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="53592-128">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53592-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="53592-129">Określa obiekt NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="53592-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="53592-130">- NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="53592-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="53592-131">Określa identyfikator sieciowej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="53592-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="53592-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="53592-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="53592-133">Konfigurowanie włączania lub wyłączania stosowania zasad sieciowych do prywatnego punktu końcowego w podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="53592-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="53592-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="53592-135">Konfigurowanie włączania lub wyłączania stosowania zasad sieciowych w prywatnej usłudze linków w podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="53592-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53592-136">-ResourceId</span></span>
<span data-ttu-id="53592-137">Określa identyfikator zasobu bramy NAT skojarzonego z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="53592-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="53592-138">-RouteTable</span></span>
<span data-ttu-id="53592-139">Określa tabelę trasy skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="53592-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="53592-140">-RouteTableId</span></span>
<span data-ttu-id="53592-141">Określa identyfikator tabeli trasy skojarzonej z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="53592-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="53592-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="53592-142">-ServiceEndpoint</span></span>
<span data-ttu-id="53592-143">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="53592-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="53592-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="53592-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="53592-145">Zasady punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="53592-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="53592-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53592-146">CommonParameters</span></span>
<span data-ttu-id="53592-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53592-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53592-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53592-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53592-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53592-149">INPUTS</span></span>

### <span data-ttu-id="53592-150">System.String</span><span class="sxs-lookup"><span data-stu-id="53592-150">System.String</span></span>

### <span data-ttu-id="53592-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53592-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="53592-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="53592-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="53592-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="53592-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="53592-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="53592-154">System.String[]</span></span>

### <span data-ttu-id="53592-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="53592-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="53592-156">Microsoft.Azure.Commands.Network.Models.PSDelegacji[]</span><span class="sxs-lookup"><span data-stu-id="53592-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="53592-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53592-157">OUTPUTS</span></span>

### <span data-ttu-id="53592-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="53592-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="53592-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53592-159">NOTES</span></span>

## <span data-ttu-id="53592-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53592-160">RELATED LINKS</span></span>

[<span data-ttu-id="53592-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="53592-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="53592-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="53592-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="53592-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="53592-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="53592-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="53592-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 144d04172f3169075a32c5e8111a90ff407532b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052195"
---
# <span data-ttu-id="96ed8-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="96ed8-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="96ed8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="96ed8-103">Umożliwia utworzenie konfiguracji podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96ed8-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="96ed8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96ed8-104">SYNTAX</span></span>

### <span data-ttu-id="96ed8-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96ed8-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96ed8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="96ed8-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96ed8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="96ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="96ed8-108">Polecenie cmdlet **New-AzVirtualNetworkSubnetConfig** umożliwia utworzenie konfiguracji podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96ed8-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="96ed8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96ed8-109">EXAMPLES</span></span>

### <span data-ttu-id="96ed8-110">1: tworzenie sieci wirtualnej z dwiema podsieciami i grupą zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="96ed8-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
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

<span data-ttu-id="96ed8-111">W tym przykładzie przedstawiono tworzenie dwóch nowych konfiguracji podsieci za pomocą polecenia cmdlet New-AzVirtualSubnetConfig, a następnie za jego pomocą Tworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96ed8-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="96ed8-112">Szablon New-AzVirtualSubnetConfig służy tylko do tworzenia reprezentacji w pamięci podsieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="96ed8-113">W tym przykładzie frontendSubnet ma CIDR 10.0.1.0/24 i odwołuje się do grupy zabezpieczeń sieci, która umożliwia dostęp do protokołu RDP.</span><span class="sxs-lookup"><span data-stu-id="96ed8-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="96ed8-114">BackendSubnet ma CIDR 10.0.2.0/24 i odwołuje się do tej samej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="96ed8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96ed8-115">PARAMETERS</span></span>

### <span data-ttu-id="96ed8-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="96ed8-116">-AddressPrefix</span></span>
<span data-ttu-id="96ed8-117">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="96ed8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ed8-118">-DefaultProfile</span></span>
<span data-ttu-id="96ed8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96ed8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96ed8-120">— Delegowanie</span><span class="sxs-lookup"><span data-stu-id="96ed8-120">-Delegation</span></span>
<span data-ttu-id="96ed8-121">Lista usług, które mają uprawnienie do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="96ed8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96ed8-122">-InputObject</span></span>
<span data-ttu-id="96ed8-123">Określa bramę NAT skojarzoną z konfiguracją podsieci</span><span class="sxs-lookup"><span data-stu-id="96ed8-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="96ed8-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="96ed8-124">-Name</span></span>
<span data-ttu-id="96ed8-125">Określa nazwę konfiguracji podsieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="96ed8-125">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="96ed8-126">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96ed8-126">-NetworkSecurityGroup</span></span>
<span data-ttu-id="96ed8-127">Określa obiekt NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="96ed8-127">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="96ed8-128">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="96ed8-128">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="96ed8-129">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-129">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="96ed8-130">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="96ed8-130">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="96ed8-131">Skonfiguruj, aby włączyć lub wyłączyć stosowanie zasad sieciowych w prywatnym punkcie końcowym podsieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-131">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="96ed8-132">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="96ed8-132">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="96ed8-133">Skonfiguruj, aby włączyć lub wyłączyć stosowanie zasad sieciowych w usłudze linku prywatnego w podsieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-133">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="96ed8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96ed8-134">-ResourceId</span></span>
<span data-ttu-id="96ed8-135">Określa identyfikator zasobu bramy NAT skojarzonego z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-135">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="96ed8-136">-Routeing</span><span class="sxs-lookup"><span data-stu-id="96ed8-136">-RouteTable</span></span>
<span data-ttu-id="96ed8-137">Określa tabelę tras skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-137">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="96ed8-138">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="96ed8-138">-RouteTableId</span></span>
<span data-ttu-id="96ed8-139">Określa identyfikator tabeli routingu skojarzonej z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="96ed8-139">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="96ed8-140">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="96ed8-140">-ServiceEndpoint</span></span>
<span data-ttu-id="96ed8-141">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="96ed8-141">Service Endpoint Value</span></span>

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

### <span data-ttu-id="96ed8-142">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="96ed8-142">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="96ed8-143">Zasady dotyczące punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="96ed8-143">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="96ed8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ed8-144">CommonParameters</span></span>
<span data-ttu-id="96ed8-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96ed8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ed8-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96ed8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ed8-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96ed8-147">INPUTS</span></span>

### <span data-ttu-id="96ed8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="96ed8-148">System.String</span></span>

### <span data-ttu-id="96ed8-149">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96ed8-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="96ed8-150">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="96ed8-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="96ed8-151">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="96ed8-151">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="96ed8-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="96ed8-152">System.String[]</span></span>

### <span data-ttu-id="96ed8-153">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="96ed8-153">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="96ed8-154">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="96ed8-154">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="96ed8-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96ed8-155">OUTPUTS</span></span>

### <span data-ttu-id="96ed8-156">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="96ed8-156">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="96ed8-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96ed8-157">NOTES</span></span>

## <span data-ttu-id="96ed8-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96ed8-158">RELATED LINKS</span></span>

[<span data-ttu-id="96ed8-159">Dodaj-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="96ed8-159">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="96ed8-160">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="96ed8-160">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="96ed8-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="96ed8-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="96ed8-162">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="96ed8-162">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)

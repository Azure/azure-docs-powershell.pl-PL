---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: ecaf236c04c24241cf285e3d8ca379d3bc52645a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872123"
---
# <span data-ttu-id="d0b81-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d0b81-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="d0b81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0b81-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b81-103">Umożliwia zaktualizowanie konfiguracji podsieci dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d0b81-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="d0b81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0b81-104">SYNTAX</span></span>

### <span data-ttu-id="d0b81-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0b81-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0b81-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0b81-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0b81-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0b81-107">DESCRIPTION</span></span>
<span data-ttu-id="d0b81-108">Polecenie cmdlet **Set-AzVirtualNetworkSubnetConfig** umożliwia zaktualizowanie konfiguracji podsieci dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d0b81-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="d0b81-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0b81-109">EXAMPLES</span></span>

### <span data-ttu-id="d0b81-110">1: modyfikowanie prefiksu adresu podsieci</span><span class="sxs-lookup"><span data-stu-id="d0b81-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="d0b81-111">W tym przykładzie jest tworzona Sieć wirtualna z pojedynczą podsiecią.</span><span class="sxs-lookup"><span data-stu-id="d0b81-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="d0b81-112">Następnie są to połączenia Set-AzVirtualNetworkSubnetConfig, aby zmodyfikować AddressPrefix podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="d0b81-113">Ma to wpływ tylko na reprezentację w pamięci wirtualnej sieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="d0b81-114">Następnie Set-AzVirtualNetwork jest wywoływana w celu zmodyfikowania sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b81-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="d0b81-115">2: Dodawanie grupy zabezpieczeń sieci do podsieci</span><span class="sxs-lookup"><span data-stu-id="d0b81-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="d0b81-116">W tym przykładzie jest tworzona Grupa zasobów z pojedynczą siecią wirtualną zawierającą tylko pojedynczą podsieć.</span><span class="sxs-lookup"><span data-stu-id="d0b81-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="d0b81-117">Następnie tworzona jest Grupa zabezpieczeń sieci z regułą dozwolonych dla ruchu RDP.</span><span class="sxs-lookup"><span data-stu-id="d0b81-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="d0b81-118">Polecenie cmdlet Set-AzVirtualNetworkSubnetConfig służy do modyfikowania reprezentacji w pamięci podsieci frontonu, tak aby wskazywała nowo utworzoną grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="d0b81-119">Następnie polecenie cmdlet Set-AzVirtualNetwork jest wywoływane w celu zapisania zmodyfikowanego stanu z powrotem do usługi.</span><span class="sxs-lookup"><span data-stu-id="d0b81-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="d0b81-120">3: dołączanie bramy NAT do podsieci</span><span class="sxs-lookup"><span data-stu-id="d0b81-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="d0b81-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0b81-121">PARAMETERS</span></span>

### <span data-ttu-id="d0b81-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d0b81-122">-AddressPrefix</span></span>
<span data-ttu-id="d0b81-123">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="d0b81-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b81-124">-DefaultProfile</span></span>
<span data-ttu-id="d0b81-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b81-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0b81-126">— Delegowanie</span><span class="sxs-lookup"><span data-stu-id="d0b81-126">-Delegation</span></span>
<span data-ttu-id="d0b81-127">Lista usług, które mają uprawnienie do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="d0b81-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d0b81-128">-InputObject</span></span>
<span data-ttu-id="d0b81-129">Określa bramę NAT skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="d0b81-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0b81-130">-Name</span></span>
<span data-ttu-id="d0b81-131">Określa nazwę konfiguracji podsieci, którą konfiguruje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0b81-131">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="d0b81-132">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d0b81-132">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d0b81-133">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="d0b81-133">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="d0b81-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d0b81-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d0b81-135">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="d0b81-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="d0b81-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="d0b81-137">Skonfiguruj, aby włączyć lub wyłączyć stosowanie zasad sieciowych w prywatnym punkcie końcowym podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="d0b81-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="d0b81-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="d0b81-139">Skonfiguruj, aby włączyć lub wyłączyć stosowanie zasad sieciowych w usłudze linku prywatnego w podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="d0b81-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0b81-140">-ResourceId</span></span>
<span data-ttu-id="d0b81-141">Określa identyfikator zasobu bramy NAT skojarzonego z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="d0b81-142">-Routeing</span><span class="sxs-lookup"><span data-stu-id="d0b81-142">-RouteTable</span></span>
<span data-ttu-id="d0b81-143">Określa obiekt tabeli routingu skojarzony z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-143">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="d0b81-144">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="d0b81-144">-RouteTableId</span></span>
<span data-ttu-id="d0b81-145">Określa identyfikator obiektu tabeli routingu, który jest skojarzony z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-145">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="d0b81-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0b81-146">-ServiceEndpoint</span></span>
<span data-ttu-id="d0b81-147">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="d0b81-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="d0b81-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d0b81-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d0b81-149">Zasady dotyczące punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="d0b81-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="d0b81-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d0b81-150">-VirtualNetwork</span></span>
<span data-ttu-id="d0b81-151">Określa obiekt **VirtualNetwork** , który zawiera konfigurację podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0b81-151">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="d0b81-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b81-152">CommonParameters</span></span>
<span data-ttu-id="d0b81-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b81-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b81-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0b81-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b81-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0b81-155">INPUTS</span></span>

### <span data-ttu-id="d0b81-156">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d0b81-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d0b81-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b81-157">System.String</span></span>

### <span data-ttu-id="d0b81-158">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d0b81-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="d0b81-159">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d0b81-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="d0b81-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="d0b81-160">System.String[]</span></span>

### <span data-ttu-id="d0b81-161">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="d0b81-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="d0b81-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="d0b81-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="d0b81-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0b81-163">OUTPUTS</span></span>

### <span data-ttu-id="d0b81-164">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d0b81-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="d0b81-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0b81-165">NOTES</span></span>

## <span data-ttu-id="d0b81-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0b81-166">RELATED LINKS</span></span>

[<span data-ttu-id="d0b81-167">Dodaj-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d0b81-167">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d0b81-168">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d0b81-168">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d0b81-169">Nowe — AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d0b81-169">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d0b81-170">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d0b81-170">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498785"
---
# <span data-ttu-id="bf605-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bf605-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="bf605-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf605-102">SYNOPSIS</span></span>
<span data-ttu-id="bf605-103">Dodaje konfigurację podsieci do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bf605-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="bf605-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf605-104">SYNTAX</span></span>

### <span data-ttu-id="bf605-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf605-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf605-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf605-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf605-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bf605-107">DESCRIPTION</span></span>
<span data-ttu-id="bf605-108">Polecenie cmdlet **Add-AzVirtualNetworkSubnetConfig** umożliwia dodanie konfiguracji podsieci do istniejącej wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="bf605-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="bf605-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf605-109">EXAMPLES</span></span>

### <span data-ttu-id="bf605-110">Przykład 1: Dodawanie podsieci do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bf605-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="bf605-111">W tym przykładzie najpierw jest tworzona Grupa zasobów jako kontener zasobów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="bf605-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="bf605-112">Następnie tworzy konfigurację podsieci i używa jej do tworzenia sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bf605-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="bf605-113">Następnie Add-AzVirtualNetworkSubnetConfig jest używana w celu dodania podsieci do reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bf605-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="bf605-114">Polecenie Set-AzVirtualNetwork umożliwia zaktualizowanie istniejącej sieci wirtualnej za pomocą nowej podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="bf605-115">Przykład 2: Dodawanie delegacji do podsieci dodawanej do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bf605-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="bf605-116">W tym przykładzie jest najpierw pobierana istniejąca sieć VNET.</span><span class="sxs-lookup"><span data-stu-id="bf605-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="bf605-117">Następnie tworzy obiekt delegowania w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bf605-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="bf605-118">Na koniec tworzy nową podsieć z tą delegacją, która jest dodawana do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bf605-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="bf605-119">Zmodyfikowana konfiguracja zostanie następnie wysłana do serwera.</span><span class="sxs-lookup"><span data-stu-id="bf605-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="bf605-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf605-120">PARAMETERS</span></span>

### <span data-ttu-id="bf605-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bf605-121">-AddressPrefix</span></span>
<span data-ttu-id="bf605-122">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="bf605-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf605-123">-DefaultProfile</span></span>
<span data-ttu-id="bf605-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf605-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf605-125">— Delegowanie</span><span class="sxs-lookup"><span data-stu-id="bf605-125">-Delegation</span></span>
<span data-ttu-id="bf605-126">Lista usług, które mają uprawnienie do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="bf605-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf605-127">-InputObject</span></span>
<span data-ttu-id="bf605-128">Określa bramę NAT skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="bf605-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="bf605-129">-IpAllocation</span></span>
<span data-ttu-id="bf605-130">Określa IpAllocations dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="bf605-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf605-131">-Name</span></span>
<span data-ttu-id="bf605-132">Określa nazwę konfiguracji podsieci do dodania.</span><span class="sxs-lookup"><span data-stu-id="bf605-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="bf605-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bf605-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="bf605-134">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="bf605-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="bf605-135">To polecenie cmdlet umożliwia dodanie konfiguracji podsieci sieci wirtualnej do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bf605-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf605-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bf605-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="bf605-137">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="bf605-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="bf605-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="bf605-139">Skonfiguruj, aby włączyć lub wyłączyć stosowanie zasad sieciowych w prywatnym punkcie końcowym podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="bf605-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="bf605-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="bf605-141">Skonfiguruj, aby włączyć lub wyłączyć stosowanie zasad sieciowych w usłudze linku prywatnego w podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="bf605-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf605-142">-ResourceId</span></span>
<span data-ttu-id="bf605-143">Określa identyfikator zasobu bramy NAT skojarzonego z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="bf605-144">-Routeing</span><span class="sxs-lookup"><span data-stu-id="bf605-144">-RouteTable</span></span>
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

### <span data-ttu-id="bf605-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="bf605-145">-RouteTableId</span></span>
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

### <span data-ttu-id="bf605-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf605-146">-ServiceEndpoint</span></span>
<span data-ttu-id="bf605-147">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="bf605-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="bf605-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bf605-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="bf605-149">Zasady dotyczące punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="bf605-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="bf605-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf605-150">-VirtualNetwork</span></span>
<span data-ttu-id="bf605-151">Określa obiekt **VirtualNetwork** , w którym ma zostać dodana konfiguracja podsieci.</span><span class="sxs-lookup"><span data-stu-id="bf605-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="bf605-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf605-152">CommonParameters</span></span>
<span data-ttu-id="bf605-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf605-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf605-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf605-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf605-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf605-155">INPUTS</span></span>

### <span data-ttu-id="bf605-156">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf605-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="bf605-157">System. String</span><span class="sxs-lookup"><span data-stu-id="bf605-157">System.String</span></span>

### <span data-ttu-id="bf605-158">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bf605-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="bf605-159">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf605-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="bf605-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="bf605-160">System.String[]</span></span>

### <span data-ttu-id="bf605-161">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="bf605-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="bf605-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="bf605-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="bf605-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf605-163">OUTPUTS</span></span>

### <span data-ttu-id="bf605-164">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf605-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bf605-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf605-165">NOTES</span></span>

## <span data-ttu-id="bf605-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf605-166">RELATED LINKS</span></span>

[<span data-ttu-id="bf605-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bf605-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="bf605-168">Nowe — AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bf605-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="bf605-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bf605-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="bf605-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bf605-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)

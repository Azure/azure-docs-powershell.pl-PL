---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241091"
---
# <span data-ttu-id="217f4-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="217f4-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="217f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="217f4-102">SYNOPSIS</span></span>
<span data-ttu-id="217f4-103">Dodaje konfigurację podsieci do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="217f4-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="217f4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="217f4-104">SYNTAX</span></span>

### <span data-ttu-id="217f4-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="217f4-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="217f4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="217f4-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="217f4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="217f4-107">DESCRIPTION</span></span>
<span data-ttu-id="217f4-108">Polecenie **cmdlet Add-AzVirtualNetworkSubnetConfig** dodaje konfigurację podsieci do istniejącej sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="217f4-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="217f4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="217f4-109">EXAMPLES</span></span>

### <span data-ttu-id="217f4-110">Przykład 1. Dodawanie podsieci do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="217f4-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="217f4-111">W tym przykładzie najpierw jest tworzona grupa zasobów jako kontener zasobów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="217f4-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="217f4-112">Następnie tworzy konfigurację podsieci i używa jej do utworzenia sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="217f4-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="217f4-113">Ten Add-AzVirtualNetworkSubnetConfig następnie służy do dodawania podsieci do reprezentacji w pamięci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="217f4-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="217f4-114">Polecenie Set-AzVirtualNetwork aktualizuje istniejącą sieć wirtualną za pomocą nowej podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="217f4-115">Przykład 2. Dodawanie delegowania do podsieci dodawanej do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="217f4-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="217f4-116">W tym przykładzie najpierw jest owijana istniejąca sieć vnet.</span><span class="sxs-lookup"><span data-stu-id="217f4-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="217f4-117">Następnie tworzy obiekt delegowania w pamięci.</span><span class="sxs-lookup"><span data-stu-id="217f4-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="217f4-118">Na koniec tworzy nową podsieci z tym delegowaniem, która jest dodawana do tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="217f4-119">Zmodyfikowana konfiguracja jest następnie wysyłana na serwer.</span><span class="sxs-lookup"><span data-stu-id="217f4-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="217f4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="217f4-120">PARAMETERS</span></span>

### <span data-ttu-id="217f4-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="217f4-121">-AddressPrefix</span></span>
<span data-ttu-id="217f4-122">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="217f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217f4-123">-DefaultProfile</span></span>
<span data-ttu-id="217f4-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="217f4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="217f4-125">—Delegowanie</span><span class="sxs-lookup"><span data-stu-id="217f4-125">-Delegation</span></span>
<span data-ttu-id="217f4-126">Lista usług z uprawnieniami do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="217f4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="217f4-127">-InputObject</span></span>
<span data-ttu-id="217f4-128">Określa bramę nat skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="217f4-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="217f4-129">-IpAllocation</span></span>
<span data-ttu-id="217f4-130">Określa alokacje IpAllocations dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="217f4-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="217f4-131">-Name</span></span>
<span data-ttu-id="217f4-132">Określa nazwę konfiguracji podsieci do dodania.</span><span class="sxs-lookup"><span data-stu-id="217f4-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="217f4-133">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="217f4-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="217f4-134">Określa obiekt **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="217f4-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="217f4-135">To polecenie cmdlet dodaje konfigurację podsieci sieci wirtualnej do obiektu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="217f4-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="217f4-136">- NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="217f4-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="217f4-137">Określa identyfikator sieciowej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="217f4-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="217f4-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="217f4-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="217f4-139">Konfigurowanie włączania lub wyłączania stosowania zasad sieciowych do prywatnego punktu końcowego w podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="217f4-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="217f4-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="217f4-141">Konfigurowanie włączania lub wyłączania stosowania zasad sieciowych w prywatnej usłudze linków w podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="217f4-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="217f4-142">-ResourceId</span></span>
<span data-ttu-id="217f4-143">Określa identyfikator zasobu bramy NAT skojarzonego z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="217f4-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="217f4-144">-RouteTable</span></span>
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

### <span data-ttu-id="217f4-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="217f4-145">-RouteTableId</span></span>
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

### <span data-ttu-id="217f4-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="217f4-146">-ServiceEndpoint</span></span>
<span data-ttu-id="217f4-147">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="217f4-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="217f4-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="217f4-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="217f4-149">Zasady punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="217f4-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="217f4-150">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="217f4-150">-VirtualNetwork</span></span>
<span data-ttu-id="217f4-151">Określa obiekt **VirtualNetwork,** w którym ma być dodawania konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="217f4-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="217f4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217f4-152">CommonParameters</span></span>
<span data-ttu-id="217f4-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="217f4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217f4-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="217f4-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217f4-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="217f4-155">INPUTS</span></span>

### <span data-ttu-id="217f4-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="217f4-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="217f4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="217f4-157">System.String</span></span>

### <span data-ttu-id="217f4-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="217f4-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="217f4-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="217f4-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="217f4-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="217f4-160">System.String[]</span></span>

### <span data-ttu-id="217f4-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="217f4-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="217f4-162">Microsoft.Azure.Commands.Network.Models.PSDelegacji[]</span><span class="sxs-lookup"><span data-stu-id="217f4-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="217f4-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="217f4-163">OUTPUTS</span></span>

### <span data-ttu-id="217f4-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="217f4-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="217f4-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="217f4-165">NOTES</span></span>

## <span data-ttu-id="217f4-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="217f4-166">RELATED LINKS</span></span>

[<span data-ttu-id="217f4-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="217f4-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="217f4-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="217f4-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="217f4-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="217f4-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="217f4-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="217f4-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)

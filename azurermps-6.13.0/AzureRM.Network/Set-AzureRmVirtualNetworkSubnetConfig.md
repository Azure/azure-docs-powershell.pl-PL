---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e8aeb73c694229e290ee96fa11d3de71bb510ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543572"
---
# <span data-ttu-id="848e0-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="848e0-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="848e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="848e0-102">SYNOPSIS</span></span>
<span data-ttu-id="848e0-103">Konfiguruje stan celu dla konfiguracji podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="848e0-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="848e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="848e0-104">SYNTAX</span></span>

### <span data-ttu-id="848e0-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="848e0-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="848e0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="848e0-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="848e0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="848e0-107">DESCRIPTION</span></span>
<span data-ttu-id="848e0-108">Polecenie cmdlet **Set-AzureRmVirtualNetworkSubnetConfig** konfiguruje stan celu dla konfiguracji podsieci w wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="848e0-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="848e0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="848e0-109">EXAMPLES</span></span>

### <span data-ttu-id="848e0-110">1: modyfikowanie prefiksu adresu podsieci</span><span class="sxs-lookup"><span data-stu-id="848e0-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="848e0-111">W tym przykładzie jest tworzona Sieć wirtualna z pojedynczą podsiecią.</span><span class="sxs-lookup"><span data-stu-id="848e0-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="848e0-112">Następnie są to połączenia Set-AzureRmVirtualNetworkSubnetConfig, aby zmodyfikować AddressPrefix podsieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="848e0-113">Ma to wpływ tylko na reprezentację w pamięci wirtualnej sieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="848e0-114">Następnie Set-AzureRmVirtualNetwork jest wywoływana w celu zmodyfikowania sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="848e0-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="848e0-115">2: Dodawanie grupy zabezpieczeń sieci do podsieci</span><span class="sxs-lookup"><span data-stu-id="848e0-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="848e0-116">W tym przykładzie jest tworzona Grupa zasobów z pojedynczą siecią wirtualną zawierającą tylko pojedynczą podsieć.</span><span class="sxs-lookup"><span data-stu-id="848e0-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="848e0-117">Następnie tworzona jest Grupa zabezpieczeń sieci z regułą dozwolonych dla ruchu RDP.</span><span class="sxs-lookup"><span data-stu-id="848e0-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="848e0-118">Polecenie cmdlet Set-AzureRmVirtualNetworkSubnetConfig służy do modyfikowania reprezentacji w pamięci podsieci frontonu, tak aby wskazywała nowo utworzoną grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="848e0-119">Następnie polecenie cmdlet Set-AzureRmVirtualNetwork jest wywoływane w celu zapisania zmodyfikowanego stanu z powrotem do usługi.</span><span class="sxs-lookup"><span data-stu-id="848e0-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="848e0-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="848e0-120">PARAMETERS</span></span>

### <span data-ttu-id="848e0-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="848e0-121">-AddressPrefix</span></span>
<span data-ttu-id="848e0-122">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="848e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848e0-123">-DefaultProfile</span></span>
<span data-ttu-id="848e0-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="848e0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="848e0-125">— Delegowanie</span><span class="sxs-lookup"><span data-stu-id="848e0-125">-Delegation</span></span>
<span data-ttu-id="848e0-126">Lista usług, które mają uprawnienie do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848e0-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="848e0-127">-Name</span></span>
<span data-ttu-id="848e0-128">Określa nazwę konfiguracji podsieci, którą konfiguruje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="848e0-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="848e0-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="848e0-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="848e0-130">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="848e0-130">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="848e0-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="848e0-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="848e0-132">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-132">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="848e0-133">-Routeing</span><span class="sxs-lookup"><span data-stu-id="848e0-133">-RouteTable</span></span>
<span data-ttu-id="848e0-134">Określa obiekt tabeli routingu skojarzony z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-134">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="848e0-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="848e0-135">-RouteTableId</span></span>
<span data-ttu-id="848e0-136">Określa identyfikator obiektu tabeli routingu, który jest skojarzony z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="848e0-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="848e0-137">-ServiceEndpoint</span></span>
<span data-ttu-id="848e0-138">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="848e0-138">Service Endpoint Value</span></span>

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

### <span data-ttu-id="848e0-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="848e0-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="848e0-140">Zasady dotyczące punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="848e0-140">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848e0-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="848e0-141">-VirtualNetwork</span></span>
<span data-ttu-id="848e0-142">Określa obiekt **VirtualNetwork** , który zawiera konfigurację podsieci.</span><span class="sxs-lookup"><span data-stu-id="848e0-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="848e0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848e0-143">CommonParameters</span></span>
<span data-ttu-id="848e0-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="848e0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848e0-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="848e0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848e0-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="848e0-146">INPUTS</span></span>

### <span data-ttu-id="848e0-147">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="848e0-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="848e0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="848e0-148">System.String</span></span>

### <span data-ttu-id="848e0-149">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="848e0-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="848e0-150">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="848e0-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="848e0-151">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="848e0-151">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="848e0-152">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSServiceEndpointPolicy; Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="848e0-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="848e0-153">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. Commands. Version = 6.7.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="848e0-153">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="848e0-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="848e0-154">OUTPUTS</span></span>

### <span data-ttu-id="848e0-155">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="848e0-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="848e0-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="848e0-156">NOTES</span></span>

## <span data-ttu-id="848e0-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="848e0-157">RELATED LINKS</span></span>

[<span data-ttu-id="848e0-158">Dodaj-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="848e0-158">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="848e0-159">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="848e0-159">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="848e0-160">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="848e0-160">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="848e0-161">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="848e0-161">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)



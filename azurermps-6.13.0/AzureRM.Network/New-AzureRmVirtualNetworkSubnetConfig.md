---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541687"
---
# <span data-ttu-id="26521-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="26521-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="26521-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26521-102">SYNOPSIS</span></span>
<span data-ttu-id="26521-103">Umożliwia utworzenie konfiguracji podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26521-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26521-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26521-104">SYNTAX</span></span>

### <span data-ttu-id="26521-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26521-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26521-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26521-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26521-107">Opis</span><span class="sxs-lookup"><span data-stu-id="26521-107">DESCRIPTION</span></span>
<span data-ttu-id="26521-108">Polecenie cmdlet **New-AzureRmVirtualNetworkSubnetConfig** umożliwia utworzenie konfiguracji podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26521-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="26521-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26521-109">EXAMPLES</span></span>

### <span data-ttu-id="26521-110">1: tworzenie sieci wirtualnej z dwiema podsieciami i grupą zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="26521-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="26521-111">W tym przykładzie przedstawiono tworzenie dwóch nowych konfiguracji podsieci za pomocą polecenia cmdlet New-AzureRmVirtualSubnetConfig, a następnie za jego pomocą Tworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26521-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="26521-112">Szablon New-AzureRmVirtualSubnetConfig służy tylko do tworzenia reprezentacji w pamięci podsieci.</span><span class="sxs-lookup"><span data-stu-id="26521-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="26521-113">W tym przykładzie frontendSubnet ma CIDR 10.0.1.0/24 i odwołuje się do grupy zabezpieczeń sieci, która umożliwia dostęp do protokołu RDP.</span><span class="sxs-lookup"><span data-stu-id="26521-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="26521-114">BackendSubnet ma CIDR 10.0.2.0/24 i odwołuje się do tej samej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="26521-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="26521-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26521-115">PARAMETERS</span></span>

### <span data-ttu-id="26521-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="26521-116">-AddressPrefix</span></span>
<span data-ttu-id="26521-117">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="26521-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="26521-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26521-118">-DefaultProfile</span></span>
<span data-ttu-id="26521-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26521-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26521-120">— Delegowanie</span><span class="sxs-lookup"><span data-stu-id="26521-120">-Delegation</span></span>
<span data-ttu-id="26521-121">Lista usług, które mają uprawnienie do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="26521-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="26521-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26521-122">-Name</span></span>
<span data-ttu-id="26521-123">Określa nazwę konfiguracji podsieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="26521-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="26521-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="26521-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="26521-125">Określa obiekt NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="26521-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="26521-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="26521-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="26521-127">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="26521-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="26521-128">-Routeing</span><span class="sxs-lookup"><span data-stu-id="26521-128">-RouteTable</span></span>
<span data-ttu-id="26521-129">Określa tabelę tras skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="26521-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="26521-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="26521-130">-RouteTableId</span></span>
<span data-ttu-id="26521-131">Określa identyfikator tabeli routingu skojarzonej z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="26521-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="26521-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="26521-132">-ServiceEndpoint</span></span>
<span data-ttu-id="26521-133">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="26521-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="26521-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="26521-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="26521-135">Zasady dotyczące punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="26521-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="26521-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26521-136">CommonParameters</span></span>
<span data-ttu-id="26521-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26521-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26521-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26521-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26521-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26521-139">INPUTS</span></span>

### <span data-ttu-id="26521-140">System. String</span><span class="sxs-lookup"><span data-stu-id="26521-140">System.String</span></span>

### <span data-ttu-id="26521-141">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="26521-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="26521-142">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="26521-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="26521-143">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="26521-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="26521-144">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSServiceEndpointPolicy; Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="26521-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="26521-145">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. Commands. Version = 6.7.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="26521-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="26521-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26521-146">OUTPUTS</span></span>

### <span data-ttu-id="26521-147">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="26521-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="26521-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26521-148">NOTES</span></span>

## <span data-ttu-id="26521-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26521-149">RELATED LINKS</span></span>

[<span data-ttu-id="26521-150">Dodaj-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="26521-150">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="26521-151">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="26521-151">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="26521-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="26521-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="26521-153">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="26521-153">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 179bfced7b73113899f525940114abb342e61f8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718728"
---
# <span data-ttu-id="f72e9-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f72e9-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="f72e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f72e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f72e9-103">Konfiguruje stan celu dla konfiguracji podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f72e9-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f72e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f72e9-104">SYNTAX</span></span>

### <span data-ttu-id="f72e9-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f72e9-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f72e9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f72e9-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f72e9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f72e9-107">DESCRIPTION</span></span>
<span data-ttu-id="f72e9-108">Polecenie cmdlet **Set-AzureRmVirtualNetworkSubnetConfig** konfiguruje stan celu dla konfiguracji podsieci w wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="f72e9-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="f72e9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f72e9-109">EXAMPLES</span></span>

### <span data-ttu-id="f72e9-110">1: modyfikowanie prefiksu adresu podsieci</span><span class="sxs-lookup"><span data-stu-id="f72e9-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="f72e9-111">W tym przykładzie jest tworzona Sieć wirtualna z pojedynczą podsiecią.</span><span class="sxs-lookup"><span data-stu-id="f72e9-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="f72e9-112">Następnie są to połączenia Set-AzureRmVirtualNetworkSubnetConfig, aby zmodyfikować AddressPrefix podsieci.</span><span class="sxs-lookup"><span data-stu-id="f72e9-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="f72e9-113">Ma to wpływ tylko na reprezentację w pamięci wirtualnej sieci.</span><span class="sxs-lookup"><span data-stu-id="f72e9-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="f72e9-114">Następnie Set-AzureRmVirtualNetwork jest wywoływana w celu zmodyfikowania sieci wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f72e9-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="f72e9-115">2: Dodawanie grupy zabezpieczeń sieci do podsieci</span><span class="sxs-lookup"><span data-stu-id="f72e9-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="f72e9-116">W tym przykładzie jest tworzona Grupa zasobów z pojedynczą siecią wirtualną zawierającą tylko pojedynczą podsieć.</span><span class="sxs-lookup"><span data-stu-id="f72e9-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="f72e9-117">Następnie tworzona jest Grupa zabezpieczeń sieci z regułą dozwolonych dla ruchu RDP.</span><span class="sxs-lookup"><span data-stu-id="f72e9-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="f72e9-118">Polecenie cmdlet Set-AzureRmVirtualNetworkSubnetConfig służy do modyfikowania reprezentacji w pamięci podsieci frontonu, tak aby wskazywała nowo utworzoną grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f72e9-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="f72e9-119">Następnie polecenie cmdlet Set-AzureRmVirtualNetwork jest wywoływane w celu zapisania zmodyfikowanego stanu z powrotem do usługi.</span><span class="sxs-lookup"><span data-stu-id="f72e9-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="f72e9-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f72e9-120">PARAMETERS</span></span>

### <span data-ttu-id="f72e9-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f72e9-121">-AddressPrefix</span></span>
<span data-ttu-id="f72e9-122">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="f72e9-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="f72e9-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f72e9-123">-Name</span></span>
<span data-ttu-id="f72e9-124">Określa nazwę konfiguracji podsieci, którą konfiguruje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f72e9-124">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="f72e9-125">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f72e9-125">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f72e9-126">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="f72e9-126">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="f72e9-127">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f72e9-127">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f72e9-128">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f72e9-128">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="f72e9-129">-Routeing</span><span class="sxs-lookup"><span data-stu-id="f72e9-129">-RouteTable</span></span>
<span data-ttu-id="f72e9-130">Określa obiekt tabeli routingu skojarzony z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f72e9-130">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="f72e9-131">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="f72e9-131">-RouteTableId</span></span>
<span data-ttu-id="f72e9-132">Określa identyfikator obiektu tabeli routingu, który jest skojarzony z grupą zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f72e9-132">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="f72e9-133">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f72e9-133">-ServiceEndpoint</span></span>
<span data-ttu-id="f72e9-134">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="f72e9-134">Service Endpoint Value</span></span>

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

### <span data-ttu-id="f72e9-135">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f72e9-135">-VirtualNetwork</span></span>
<span data-ttu-id="f72e9-136">Określa obiekt **VirtualNetwork** , który zawiera konfigurację podsieci.</span><span class="sxs-lookup"><span data-stu-id="f72e9-136">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="f72e9-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72e9-137">-DefaultProfile</span></span>
<span data-ttu-id="f72e9-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f72e9-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f72e9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72e9-139">CommonParameters</span></span>
<span data-ttu-id="f72e9-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72e9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72e9-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72e9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72e9-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f72e9-142">INPUTS</span></span>

### <span data-ttu-id="f72e9-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f72e9-143">PSVirtualNetwork</span></span>
<span data-ttu-id="f72e9-144">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="f72e9-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="f72e9-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f72e9-145">OUTPUTS</span></span>

### <span data-ttu-id="f72e9-146">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f72e9-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f72e9-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f72e9-147">NOTES</span></span>

## <span data-ttu-id="f72e9-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f72e9-148">RELATED LINKS</span></span>

[<span data-ttu-id="f72e9-149">Dodaj-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f72e9-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f72e9-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f72e9-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f72e9-151">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f72e9-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f72e9-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f72e9-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: be1b0f81aa33fb0f1368e5730e80f41b9fdcabb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548888"
---
# <span data-ttu-id="f7baf-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f7baf-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="f7baf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7baf-102">SYNOPSIS</span></span>
<span data-ttu-id="f7baf-103">Umożliwia utworzenie konfiguracji podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7baf-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7baf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7baf-104">SYNTAX</span></span>

### <span data-ttu-id="f7baf-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f7baf-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7baf-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7baf-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7baf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f7baf-107">DESCRIPTION</span></span>
<span data-ttu-id="f7baf-108">Polecenie cmdlet **New-AzureRmVirtualNetworkSubnetConfig** umożliwia utworzenie konfiguracji podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7baf-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="f7baf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7baf-109">EXAMPLES</span></span>

### <span data-ttu-id="f7baf-110">1: tworzenie sieci wirtualnej z dwiema podsieciami i grupą zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="f7baf-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="f7baf-111">W tym przykładzie przedstawiono tworzenie dwóch nowych konfiguracji podsieci za pomocą polecenia cmdlet New-AzureRmVirtualSubnetConfig, a następnie za jego pomocą Tworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7baf-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="f7baf-112">Szablon New-AzureRmVirtualSubnetConfig służy tylko do tworzenia reprezentacji w pamięci podsieci.</span><span class="sxs-lookup"><span data-stu-id="f7baf-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="f7baf-113">W tym przykładzie frontendSubnet ma CIDR 10.0.1.0/24 i odwołuje się do grupy zabezpieczeń sieci, która umożliwia dostęp do protokołu RDP.</span><span class="sxs-lookup"><span data-stu-id="f7baf-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="f7baf-114">BackendSubnet ma CIDR 10.0.2.0/24 i odwołuje się do tej samej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f7baf-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="f7baf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7baf-115">PARAMETERS</span></span>

### <span data-ttu-id="f7baf-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f7baf-116">-AddressPrefix</span></span>
<span data-ttu-id="f7baf-117">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="f7baf-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7baf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7baf-118">-DefaultProfile</span></span>
<span data-ttu-id="f7baf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7baf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7baf-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7baf-120">-Name</span></span>
<span data-ttu-id="f7baf-121">Określa nazwę konfiguracji podsieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f7baf-121">Specifies the name of the subnet configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7baf-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7baf-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f7baf-123">Określa obiekt NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="f7baf-123">Specifies a NetworkSecurityGroup object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7baf-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f7baf-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f7baf-125">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f7baf-125">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7baf-126">-Routeing</span><span class="sxs-lookup"><span data-stu-id="f7baf-126">-RouteTable</span></span>
<span data-ttu-id="f7baf-127">Określa tabelę tras skojarzoną z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="f7baf-127">Specifies the route table associated with the subnet configuration.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7baf-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="f7baf-128">-RouteTableId</span></span>
<span data-ttu-id="f7baf-129">Określa identyfikator tabeli routingu skojarzonej z konfiguracją podsieci.</span><span class="sxs-lookup"><span data-stu-id="f7baf-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7baf-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7baf-130">-ServiceEndpoint</span></span>
<span data-ttu-id="f7baf-131">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="f7baf-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="f7baf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7baf-132">CommonParameters</span></span>
<span data-ttu-id="f7baf-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7baf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7baf-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7baf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7baf-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7baf-135">INPUTS</span></span>

### <span data-ttu-id="f7baf-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f7baf-136">None</span></span>
<span data-ttu-id="f7baf-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f7baf-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7baf-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7baf-138">OUTPUTS</span></span>

### <span data-ttu-id="f7baf-139">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f7baf-139">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="f7baf-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7baf-140">NOTES</span></span>

## <span data-ttu-id="f7baf-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7baf-141">RELATED LINKS</span></span>

[<span data-ttu-id="f7baf-142">Dodaj-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f7baf-142">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f7baf-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f7baf-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f7baf-144">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f7baf-144">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f7baf-145">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f7baf-145">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)



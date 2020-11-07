---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1129b24c69dc362ea4d700be28a0823afa860885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718817"
---
# <span data-ttu-id="1ef32-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ef32-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="1ef32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ef32-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef32-103">Dodaje konfigurację podsieci do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ef32-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ef32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ef32-104">SYNTAX</span></span>

### <span data-ttu-id="1ef32-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1ef32-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ef32-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ef32-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ef32-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1ef32-107">DESCRIPTION</span></span>
<span data-ttu-id="1ef32-108">Polecenie cmdlet **Add-AzureRmVirtualNetworkSubnetConfig** umożliwia dodanie konfiguracji podsieci do istniejącej wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef32-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="1ef32-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ef32-109">EXAMPLES</span></span>

### <span data-ttu-id="1ef32-110">1: Dodawanie podsieci do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1ef32-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="1ef32-111">W tym przykładzie najpierw jest tworzona Grupa zasobów jako kontener zasobów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="1ef32-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="1ef32-112">Następnie tworzy konfigurację podsieci i używa jej do tworzenia sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ef32-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="1ef32-113">Następnie Add-AzureRmVirtualNetworkSubnetConfig jest używana w celu dodania podsieci do reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="1ef32-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="1ef32-114">Polecenie Set-AzureRmVirtualNetwork umożliwia zaktualizowanie istniejącej sieci wirtualnej za pomocą nowej podsieci.</span><span class="sxs-lookup"><span data-stu-id="1ef32-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="1ef32-115">2: Dodawanie delegacji do podsieci dodawanej do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1ef32-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="1ef32-116">W tym przykładzie jest najpierw pobierana istniejąca sieć VNET.</span><span class="sxs-lookup"><span data-stu-id="1ef32-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="1ef32-117">Następnie tworzy obiekt delegowania w pamięci.</span><span class="sxs-lookup"><span data-stu-id="1ef32-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="1ef32-118">Na koniec tworzy nową podsieć z tą delegacją, która jest dodawana do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ef32-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="1ef32-119">Zmodyfikowana konfiguracja zostanie następnie wysłana do serwera.</span><span class="sxs-lookup"><span data-stu-id="1ef32-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="1ef32-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ef32-120">PARAMETERS</span></span>

### <span data-ttu-id="1ef32-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1ef32-121">-AddressPrefix</span></span>
<span data-ttu-id="1ef32-122">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="1ef32-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="1ef32-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef32-123">-DefaultProfile</span></span>
<span data-ttu-id="1ef32-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef32-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ef32-125">— Delegowanie</span><span class="sxs-lookup"><span data-stu-id="1ef32-125">-Delegation</span></span>
<span data-ttu-id="1ef32-126">Lista usług, które mają uprawnienie do wykonywania operacji w tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="1ef32-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="1ef32-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ef32-127">-Name</span></span>
<span data-ttu-id="1ef32-128">Określa nazwę konfiguracji podsieci do dodania.</span><span class="sxs-lookup"><span data-stu-id="1ef32-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="1ef32-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ef32-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1ef32-130">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="1ef32-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="1ef32-131">To polecenie cmdlet umożliwia dodanie konfiguracji podsieci sieci wirtualnej do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1ef32-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ef32-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1ef32-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="1ef32-133">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="1ef32-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="1ef32-134">-Routeing</span><span class="sxs-lookup"><span data-stu-id="1ef32-134">-RouteTable</span></span>
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

### <span data-ttu-id="1ef32-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="1ef32-135">-RouteTableId</span></span>
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

### <span data-ttu-id="1ef32-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ef32-136">-ServiceEndpoint</span></span>
<span data-ttu-id="1ef32-137">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="1ef32-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="1ef32-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1ef32-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="1ef32-139">Zasady dotyczące punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="1ef32-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="1ef32-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ef32-140">-VirtualNetwork</span></span>
<span data-ttu-id="1ef32-141">Określa obiekt **VirtualNetwork** , w którym ma zostać dodana konfiguracja podsieci.</span><span class="sxs-lookup"><span data-stu-id="1ef32-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="1ef32-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef32-142">CommonParameters</span></span>
<span data-ttu-id="1ef32-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef32-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef32-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef32-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef32-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ef32-145">INPUTS</span></span>

### <span data-ttu-id="1ef32-146">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ef32-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="1ef32-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1ef32-147">System.String</span></span>

### <span data-ttu-id="1ef32-148">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ef32-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="1ef32-149">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ef32-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="1ef32-150">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1ef32-150">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1ef32-151">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSServiceEndpointPolicy; Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1ef32-151">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1ef32-152">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. Commands. Version = 6.7.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1ef32-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1ef32-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ef32-153">OUTPUTS</span></span>

### <span data-ttu-id="1ef32-154">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ef32-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="1ef32-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ef32-155">NOTES</span></span>

## <span data-ttu-id="1ef32-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ef32-156">RELATED LINKS</span></span>

[<span data-ttu-id="1ef32-157">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ef32-157">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1ef32-158">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ef32-158">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1ef32-159">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ef32-159">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1ef32-160">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ef32-160">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)



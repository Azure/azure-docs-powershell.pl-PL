---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 9b5718dc7d0931a5a99e8f76ce4376b0753bc571
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718162"
---
# <span data-ttu-id="02294-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="02294-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="02294-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02294-102">SYNOPSIS</span></span>
<span data-ttu-id="02294-103">Dodaje konfigurację podsieci do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02294-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02294-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02294-104">SYNTAX</span></span>

### <span data-ttu-id="02294-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02294-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02294-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="02294-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02294-107">Opis</span><span class="sxs-lookup"><span data-stu-id="02294-107">DESCRIPTION</span></span>
<span data-ttu-id="02294-108">Polecenie cmdlet **Add-AzureRmVirtualNetworkSubnetConfig** umożliwia dodanie konfiguracji podsieci do istniejącej wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="02294-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="02294-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02294-109">EXAMPLES</span></span>

### <span data-ttu-id="02294-110">1: Dodawanie podsieci do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="02294-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="02294-111">W tym przykładzie najpierw jest tworzona Grupa zasobów jako kontener zasobów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="02294-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="02294-112">Następnie tworzy konfigurację podsieci i używa jej do tworzenia sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02294-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="02294-113">Następnie Add-AzureRmVirtualNetworkSubnetConfig jest używana w celu dodania podsieci do reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="02294-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="02294-114">Polecenie Set-AzureRmVirtualNetwork umożliwia zaktualizowanie istniejącej sieci wirtualnej za pomocą nowej podsieci.</span><span class="sxs-lookup"><span data-stu-id="02294-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="02294-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02294-115">PARAMETERS</span></span>

### <span data-ttu-id="02294-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="02294-116">-AddressPrefix</span></span>
<span data-ttu-id="02294-117">Określa zakres adresów IP dla konfiguracji podsieci.</span><span class="sxs-lookup"><span data-stu-id="02294-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="02294-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02294-118">-Name</span></span>
<span data-ttu-id="02294-119">Określa nazwę konfiguracji podsieci do dodania.</span><span class="sxs-lookup"><span data-stu-id="02294-119">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="02294-120">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="02294-120">-NetworkSecurityGroup</span></span>
<span data-ttu-id="02294-121">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="02294-121">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="02294-122">To polecenie cmdlet umożliwia dodanie konfiguracji podsieci sieci wirtualnej do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="02294-122">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="02294-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="02294-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="02294-124">Określa identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="02294-124">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="02294-125">-Routeing</span><span class="sxs-lookup"><span data-stu-id="02294-125">-RouteTable</span></span>
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

### <span data-ttu-id="02294-126">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="02294-126">-RouteTableId</span></span>
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

### <span data-ttu-id="02294-127">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="02294-127">-ServiceEndpoint</span></span>
<span data-ttu-id="02294-128">Wartość punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="02294-128">Service Endpoint Value</span></span>

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

### <span data-ttu-id="02294-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02294-129">-VirtualNetwork</span></span>
<span data-ttu-id="02294-130">Określa obiekt **VirtualNetwork** , w którym ma zostać dodana konfiguracja podsieci.</span><span class="sxs-lookup"><span data-stu-id="02294-130">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="02294-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02294-131">-DefaultProfile</span></span>
<span data-ttu-id="02294-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02294-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02294-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02294-133">CommonParameters</span></span>
<span data-ttu-id="02294-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02294-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02294-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02294-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02294-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02294-136">INPUTS</span></span>

### <span data-ttu-id="02294-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02294-137">PSVirtualNetwork</span></span>
<span data-ttu-id="02294-138">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="02294-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="02294-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02294-139">OUTPUTS</span></span>

### <span data-ttu-id="02294-140">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02294-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="02294-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02294-141">NOTES</span></span>

## <span data-ttu-id="02294-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02294-142">RELATED LINKS</span></span>

[<span data-ttu-id="02294-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="02294-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="02294-144">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="02294-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="02294-145">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="02294-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="02294-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="02294-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)



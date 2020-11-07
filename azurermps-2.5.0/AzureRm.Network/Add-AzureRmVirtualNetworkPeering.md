---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: 1bf784a94d3f4a03c380f114064fa3f1e399e379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899307"
---
# <span data-ttu-id="ae526-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ae526-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="ae526-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae526-102">SYNOPSIS</span></span>
<span data-ttu-id="ae526-103">Tworzy komunikację między dwiema sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="ae526-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae526-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae526-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae526-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae526-105">DESCRIPTION</span></span>
<span data-ttu-id="ae526-106">Polecenie cmdlet **Add-AzureRmVirtualNetworkPeering** umożliwia utworzenie komunikacji równorzędnej między dwiema sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="ae526-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="ae526-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae526-107">EXAMPLES</span></span>

### <span data-ttu-id="ae526-108">Przykład 1: Tworzenie komunikacji równorzędnej między dwiema sieciami wirtualnymi w tym samym regionie</span><span class="sxs-lookup"><span data-stu-id="ae526-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="ae526-109">Należy pamiętać, że w celu działania komunikacji równorzędnej należy utworzyć link do komunikacji równorzędnej z vnet1 na vnet2 i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="ae526-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="ae526-110">Przykład 2: Tworzenie komunikacji równorzędnej między dwiema sieciami wirtualnymi w różnych regionach</span><span class="sxs-lookup"><span data-stu-id="ae526-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="ae526-111">W tym miejscu "myVnet1" w Stanach Zjednoczonych centrali zachodniej jest to peering z "myVnet2" w centrali Kanada.</span><span class="sxs-lookup"><span data-stu-id="ae526-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="ae526-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae526-112">PARAMETERS</span></span>

### <span data-ttu-id="ae526-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="ae526-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="ae526-114">Wskazuje, że to polecenie cmdlet umożliwia przekazanie ruchu z maszyn wirtualnych w zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae526-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae526-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="ae526-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="ae526-116">Flaga zezwalająca na gatewayLinks być używana w łączu zdalnej sieci wirtualnej z tą siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="ae526-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae526-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae526-117">-AsJob</span></span>
<span data-ttu-id="ae526-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ae526-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae526-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ae526-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="ae526-120">Wskazuje, że to polecenie cmdlet blokuje maszyny wirtualne w połączonej wirtualnej przestrzeni sieciowej, aby uzyskać dostęp do wszystkich maszyn wirtualnych w lokalnej wirtualnej przestrzeni sieciowej.</span><span class="sxs-lookup"><span data-stu-id="ae526-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae526-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae526-121">-DefaultProfile</span></span>
<span data-ttu-id="ae526-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae526-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae526-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae526-123">-Name</span></span>
<span data-ttu-id="ae526-124">Określa nazwę komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae526-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="ae526-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ae526-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="ae526-126">Określa identyfikator zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae526-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae526-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="ae526-127">-UseRemoteGateways</span></span>
<span data-ttu-id="ae526-128">Wskazuje, że to polecenie cmdlet zezwala na bramy zdalne w tej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae526-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae526-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ae526-129">-VirtualNetwork</span></span>
<span data-ttu-id="ae526-130">Określa nadrzędną sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="ae526-130">Specifies the parent virtual network.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae526-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae526-131">CommonParameters</span></span>
<span data-ttu-id="ae526-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae526-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae526-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae526-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae526-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae526-134">INPUTS</span></span>

### <span data-ttu-id="ae526-135">Ciąg</span><span class="sxs-lookup"><span data-stu-id="ae526-135">String</span></span>
<span data-ttu-id="ae526-136">Parametr "RemoteVirtualNetworkId" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="ae526-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="ae526-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ae526-137">PSVirtualNetwork</span></span>
<span data-ttu-id="ae526-138">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ae526-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="ae526-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae526-139">OUTPUTS</span></span>

### <span data-ttu-id="ae526-140">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ae526-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="ae526-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae526-141">NOTES</span></span>

## <span data-ttu-id="ae526-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae526-142">RELATED LINKS</span></span>

[<span data-ttu-id="ae526-143">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ae526-143">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="ae526-144">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ae526-144">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="ae526-145">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ae526-145">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="ae526-146">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ae526-146">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)



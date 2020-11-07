---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: c4dbac761b9dd73a7d8d2b73f3d62975f1d7611f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870315"
---
# <span data-ttu-id="48507-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="48507-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="48507-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48507-102">SYNOPSIS</span></span>
<span data-ttu-id="48507-103">Tworzy komunikację między dwiema sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="48507-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="48507-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48507-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48507-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48507-105">DESCRIPTION</span></span>
<span data-ttu-id="48507-106">Polecenie cmdlet **Add-AzVirtualNetworkPeering** umożliwia utworzenie komunikacji równorzędnej między dwiema sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="48507-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="48507-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48507-107">EXAMPLES</span></span>

### <span data-ttu-id="48507-108">Przykład 1: Tworzenie komunikacji równorzędnej między dwiema sieciami wirtualnymi w tym samym regionie</span><span class="sxs-lookup"><span data-stu-id="48507-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="48507-109">Należy pamiętać, że w celu działania komunikacji równorzędnej należy utworzyć link do komunikacji równorzędnej z vnet1 na vnet2 i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="48507-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="48507-110">Przykład 2: Tworzenie komunikacji równorzędnej między dwiema sieciami wirtualnymi w różnych regionach</span><span class="sxs-lookup"><span data-stu-id="48507-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location canadacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="48507-111">W tym miejscu "myVnet1" w Stanach Zjednoczonych centrali zachodniej jest to peering z "myVnet2" w centrali Kanada.</span><span class="sxs-lookup"><span data-stu-id="48507-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="48507-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48507-112">PARAMETERS</span></span>

### <span data-ttu-id="48507-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="48507-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="48507-114">Wskazuje, że to polecenie cmdlet umożliwia przekazanie ruchu z maszyn wirtualnych w zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48507-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48507-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="48507-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="48507-116">Flaga zezwalająca na gatewayLinks być używana w łączu zdalnej sieci wirtualnej z tą siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="48507-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48507-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48507-117">-AsJob</span></span>
<span data-ttu-id="48507-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="48507-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48507-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="48507-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="48507-120">Wskazuje, że to polecenie cmdlet blokuje maszyny wirtualne w połączonej wirtualnej przestrzeni sieciowej, aby uzyskać dostęp do wszystkich maszyn wirtualnych w lokalnej wirtualnej przestrzeni sieciowej.</span><span class="sxs-lookup"><span data-stu-id="48507-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48507-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48507-121">-DefaultProfile</span></span>
<span data-ttu-id="48507-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48507-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48507-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48507-123">-Name</span></span>
<span data-ttu-id="48507-124">Określa nazwę komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48507-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="48507-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="48507-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="48507-126">Określa identyfikator zdalnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48507-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48507-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="48507-127">-UseRemoteGateways</span></span>
<span data-ttu-id="48507-128">Wskazuje, że to polecenie cmdlet zezwala na bramy zdalne w tej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48507-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48507-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48507-129">-VirtualNetwork</span></span>
<span data-ttu-id="48507-130">Określa nadrzędną sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="48507-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="48507-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48507-131">CommonParameters</span></span>
<span data-ttu-id="48507-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48507-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48507-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48507-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48507-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48507-134">INPUTS</span></span>

### <span data-ttu-id="48507-135">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48507-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="48507-136">System. String</span><span class="sxs-lookup"><span data-stu-id="48507-136">System.String</span></span>

## <span data-ttu-id="48507-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48507-137">OUTPUTS</span></span>

### <span data-ttu-id="48507-138">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="48507-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="48507-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48507-139">NOTES</span></span>

## <span data-ttu-id="48507-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48507-140">RELATED LINKS</span></span>

[<span data-ttu-id="48507-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48507-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="48507-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="48507-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="48507-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="48507-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="48507-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="48507-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)

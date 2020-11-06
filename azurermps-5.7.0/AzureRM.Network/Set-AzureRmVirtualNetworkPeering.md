---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a8af220313d0e6bbd03d35aa60d235651b19704c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542475"
---
# <span data-ttu-id="0c7d0-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0c7d0-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="0c7d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7d0-103">Umożliwia skonfigurowanie komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c7d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c7d0-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c7d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c7d0-105">DESCRIPTION</span></span>
<span data-ttu-id="0c7d0-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkPeering** umożliwia skonfigurowanie komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="0c7d0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c7d0-107">EXAMPLES</span></span>

### <span data-ttu-id="0c7d0-108">Przykład 1: Zmienianie konfiguracji ruchu przekierowanego dla komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0c7d0-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="0c7d0-109">Przykład 2: zmienianie dostępu do sieci wirtualnej dla komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0c7d0-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="0c7d0-110">Przykład 3: Zmienianie konfiguracji właściwości tranzytu bramy dla komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0c7d0-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="0c7d0-111">Przykład 4: używanie bram zdalnych w komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0c7d0-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="0c7d0-112">Zmieniając tę właściwość na $True, można użyć bramy VNet w sieci równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="0c7d0-113">Jednak w sieci wirtualnej sieci równorzędnej musi być skonfigurowana brama, a **AllowGatewayTransit** musi mieć wartość $true.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="0c7d0-114">Tej właściwości nie można użyć, jeśli Brama została już skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="0c7d0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c7d0-115">PARAMETERS</span></span>

### <span data-ttu-id="0c7d0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c7d0-116">-AsJob</span></span>
<span data-ttu-id="0c7d0-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0c7d0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c7d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7d0-118">-DefaultProfile</span></span>
<span data-ttu-id="0c7d0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c7d0-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0c7d0-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="0c7d0-121">Określa komunikację między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-121">Specifies the virtual network peering.</span></span>

```yaml
Type: PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7d0-122">CommonParameters</span></span>
<span data-ttu-id="0c7d0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7d0-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c7d0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7d0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c7d0-125">INPUTS</span></span>

### <span data-ttu-id="0c7d0-126">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0c7d0-126">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="0c7d0-127">Parametr "VirtualNetworkPeering" akceptuje wartość typu "PSVirtualNetworkPeering" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0c7d0-127">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="0c7d0-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c7d0-128">OUTPUTS</span></span>

### <span data-ttu-id="0c7d0-129">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0c7d0-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="0c7d0-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c7d0-130">NOTES</span></span>

## <span data-ttu-id="0c7d0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c7d0-131">RELATED LINKS</span></span>

[<span data-ttu-id="0c7d0-132">Dodaj-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0c7d0-132">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="0c7d0-133">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0c7d0-133">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="0c7d0-134">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0c7d0-134">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)



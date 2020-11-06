---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527381"
---
# <span data-ttu-id="b5b3f-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b5b3f-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="b5b3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b3f-103">Umożliwia skonfigurowanie komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5b3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5b3f-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5b3f-105">DESCRIPTION</span></span>
<span data-ttu-id="b5b3f-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkPeering** umożliwia skonfigurowanie komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="b5b3f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5b3f-107">EXAMPLES</span></span>

### <span data-ttu-id="b5b3f-108">Przykład 1: Zmienianie konfiguracji ruchu przekierowanego dla komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b5b3f-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="b5b3f-109">Przykład 2: zmienianie dostępu do sieci wirtualnej dla komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b5b3f-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="b5b3f-110">Przykład 3: Zmienianie konfiguracji właściwości tranzytu bramy dla komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b5b3f-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="b5b3f-111">Przykład 4: używanie bram zdalnych w komunikacji równorzędnej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b5b3f-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="b5b3f-112">Zmieniając tę właściwość na $True, można użyć bramy VNet w sieci równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="b5b3f-113">Jednak w sieci wirtualnej sieci równorzędnej musi być skonfigurowana brama, a **AllowGatewayTransit** musi mieć wartość $true.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="b5b3f-114">Tej właściwości nie można użyć, jeśli Brama została już skonfigurowana.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="b5b3f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5b3f-115">PARAMETERS</span></span>

### <span data-ttu-id="b5b3f-116">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b5b3f-116">-VirtualNetworkPeering</span></span>
<span data-ttu-id="b5b3f-117">Określa komunikację między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-117">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b3f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b3f-118">-DefaultProfile</span></span>
<span data-ttu-id="b5b3f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5b3f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b3f-120">CommonParameters</span></span>
<span data-ttu-id="b5b3f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b3f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b3f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b3f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b3f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5b3f-123">INPUTS</span></span>

### <span data-ttu-id="b5b3f-124">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b5b3f-124">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="b5b3f-125">Parametr "VirtualNetworkPeering" akceptuje wartość typu "PSVirtualNetworkPeering" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b5b3f-125">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="b5b3f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5b3f-126">OUTPUTS</span></span>

### <span data-ttu-id="b5b3f-127">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b5b3f-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="b5b3f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5b3f-128">NOTES</span></span>

## <span data-ttu-id="b5b3f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5b3f-129">RELATED LINKS</span></span>

[<span data-ttu-id="b5b3f-130">Dodaj-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b5b3f-130">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="b5b3f-131">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b5b3f-131">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="b5b3f-132">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b5b3f-132">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


